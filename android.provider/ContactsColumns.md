# ContactsContract.ContactsColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ContactsColumns

Kotlin| [Java](../android/provider/ContactsContract.ContactsColumns.md) 
| --- | --- |

```
protected interface ContactsColumns
```

| [android.provider.ContactsContract.ContactsColumns](../android/provider/ContactsContract.ContactsColumns.md) |

| Known Direct Subclasses [ContactsContract.Contacts](../android/provider/ContactsContract.Contacts.md), [ContactsContract.Contacts.AggregationSuggestions](../android/provider/ContactsContract.Contacts.AggregationSuggestions.md), [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md), [ContactsContract.PhoneLookup](../android/provider/ContactsContract.PhoneLookup.md), [ContactsContract.Profile](../android/provider/ContactsContract.Profile.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts](../android/provider/ContactsContract.Contacts.md) | Constants for the contacts table, which contains a record per aggregate of raw contacts representing the same person. | | [ContactsContract.Contacts.AggregationSuggestions](../android/provider/ContactsContract.Contacts.AggregationSuggestions.md) | A*read-only*sub-directory of a single contact aggregate that contains all aggregation suggestions (other contacts). | | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) | Combines all columns returned by [ContactsContract.Data](../android/provider/ContactsContract.Data.md) table queries. | | [ContactsContract.PhoneLookup](../android/provider/ContactsContract.PhoneLookup.md) | A table that represents the result of looking up a phone number, for example for caller ID. | | [ContactsContract.Profile](../android/provider/ContactsContract.Profile.md) | Constants for the user's profile data, which is represented as a single contact on the device that represents the user. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md), [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md), [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md), [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md), [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md), [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md), [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md), [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md), [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md), [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md), [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md), [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) and [Email](../android/provider/ContactsContract.CommonDataKinds.Email.md)). | | [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](../android/provider/ContactsContract.CommonDataKinds.Relation.md) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](../android/provider/ContactsContract.CommonDataKinds.SipAddress.md) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](../android/provider/ContactsContract.CommonDataKinds.StructuredName.md) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](../android/provider/ContactsContract.CommonDataKinds.StructuredPostal.md) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](../android/provider/ContactsContract.CommonDataKinds.Website.md) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](../android/provider/ContactsContract.Contacts.Photo.md) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](../android/provider/ContactsContract.Data.md) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Columns of [ContactsContract.Contacts](../android/provider/ContactsContract.Contacts.md) that refer to intrinsic properties of the contact, as opposed to the user-specified options found in [ContactOptionsColumns](../android/provider/ContactsContract.ContactOptionsColumns.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTACT_LAST_UPDATED_TIMESTAMP](../android/provider/ContactsContract.ContactsColumns.md) Timestamp (milliseconds since epoch) of when this contact was last updated. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DISPLAY_NAME](../android/provider/ContactsContract.ContactsColumns.md) The display name for the contact. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [HAS_PHONE_NUMBER](../android/provider/ContactsContract.ContactsColumns.md) An indicator of whether this contact has at least one phone number. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IN_DEFAULT_DIRECTORY](../android/provider/ContactsContract.ContactsColumns.md) Flag that reflects whether the contact exists inside the default directory. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IN_VISIBLE_GROUP](../android/provider/ContactsContract.ContactsColumns.md) Flag that reflects the [Groups.GROUP_VISIBLE](../android/provider/ContactsContract.GroupsColumns.md) state of any [CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) for this contact. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_USER_PROFILE](../android/provider/ContactsContract.ContactsColumns.md) Flag that reflects whether this contact represents the user's personal profile entry. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LOOKUP_KEY](../android/provider/ContactsContract.ContactsColumns.md) An opaque value that contains hints on how to find the contact if its row id changed as a result of a sync or aggregation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME_RAW_CONTACT_ID](../android/provider/ContactsContract.ContactsColumns.md) Reference to the row in the RawContacts table holding the contact name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_FILE_ID](../android/provider/ContactsContract.ContactsColumns.md) Photo file ID of the full-size photo. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_ID](../android/provider/ContactsContract.ContactsColumns.md) Reference to the row in the data table holding the photo. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_THUMBNAIL_URI](../android/provider/ContactsContract.ContactsColumns.md) A URI that can be used to retrieve a thumbnail of the contact's photo. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PHOTO_URI](../android/provider/ContactsContract.ContactsColumns.md) A URI that can be used to retrieve the contact's full-size photo. |
| --- | --- |

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

Flag that reflects the [Groups.GROUP_VISIBLE](../android/provider/ContactsContract.GroupsColumns.md) state of any [CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) for this contact. 

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

Photo file ID of the full-size photo. If present, this will be used to populate [PHOTO_URI](../android/provider/ContactsContract.ContactsColumns.md). The ID can also be used with [ContactsContract.DisplayPhoto.CONTENT_URI](../android/provider/ContactsContract.DisplayPhoto.md) to create a URI to the photo. If this is present, [PHOTO_ID](../android/provider/ContactsContract.ContactsColumns.md) is also guaranteed to be populated.

Type: INTEGER 

 Value: "photo_file_id"

### PHOTO_ID

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_ID: String
```

Reference to the row in the data table holding the photo. A photo can be referred to either by ID (this field) or by URI (see [PHOTO_THUMBNAIL_URI](../android/provider/ContactsContract.ContactsColumns.md) and [PHOTO_URI](../android/provider/ContactsContract.ContactsColumns.md)). If PHOTO_ID is null, consult [PHOTO_URI](../android/provider/ContactsContract.ContactsColumns.md) or [PHOTO_THUMBNAIL_URI](../android/provider/ContactsContract.ContactsColumns.md), which is a more generic mechanism for referencing the contact photo, especially for contacts returned by non-local directories (see [Directory](../android/provider/ContactsContract.Directory.md)).

Type: INTEGER REFERENCES data(_id) 

 Value: "photo_id"

### PHOTO_THUMBNAIL_URI

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_THUMBNAIL_URI: String
```

A URI that can be used to retrieve a thumbnail of the contact's photo. A photo can be referred to either by a URI (this field or [PHOTO_URI](../android/provider/ContactsContract.ContactsColumns.md)) or by ID (see [PHOTO_ID](../android/provider/ContactsContract.ContactsColumns.md)). If PHOTO_ID is not null, PHOTO_URI and PHOTO_THUMBNAIL_URI shall not be null (but not necessarily vice versa). If the content provider does not differentiate between full-size photos and thumbnail photos, PHOTO_THUMBNAIL_URI and [PHOTO_URI](../android/provider/ContactsContract.ContactsColumns.md) can contain the same value, but either both shall be null or both not null.

Type: TEXT 

 Value: "photo_thumb_uri"

### PHOTO_URI

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHOTO_URI: String
```

A URI that can be used to retrieve the contact's full-size photo. If PHOTO_FILE_ID is not null, this will be populated with a URI based off [ContactsContract.DisplayPhoto.CONTENT_URI](../android/provider/ContactsContract.DisplayPhoto.md). Otherwise, this will be populated with the same value as [PHOTO_THUMBNAIL_URI](../android/provider/ContactsContract.ContactsColumns.md). A photo can be referred to either by a URI (this field) or by ID (see [PHOTO_ID](../android/provider/ContactsContract.ContactsColumns.md)). If either PHOTO_FILE_ID or PHOTO_ID is not null, PHOTO_URI and PHOTO_THUMBNAIL_URI shall not be null (but not necessarily vice versa). Thus using PHOTO_URI is a more robust method of retrieving contact photos.

Type: TEXT 

 Value: "photo_uri"
