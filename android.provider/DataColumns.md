# ContactsContract.DataColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.DataColumns "View this page in Java") 

```
protected interface DataColumns
```

| [android.provider.ContactsContract.DataColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#) |

| Known Direct Subclasses [ContactsContract.Contacts.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Data), [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins), [ContactsContract.RawContacts.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts.Data), [ContactsContract.RawContacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts.Entity), [ContactsContract.RawContactsEntity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsEntity) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Data) | A sub-directory of a single contact that contains all of the constituent raw contact [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins) | Combines all columns returned by [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) table queries. | | [ContactsContract.RawContacts.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts.Data) | A sub-directory of a single raw contact that contains all of its [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.RawContacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts.Entity) | A sub-directory of a single raw contact that contains all of its [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.RawContactsEntity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContactsEntity) | Constants for the raw contacts entities table, which can be thought of as an outer join of the raw_contacts table with the data table. | |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable), [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables), [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email), [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event), [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership), [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity), [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im), [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname), [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note), [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization), [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone), [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) and [Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email)). | | [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Relation) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.SipAddress) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredName) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Website) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Photo) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) | Constants for the data table, which contains data points tied to a raw contact. | |

Columns in the Data table.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CARRIER_PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#CARRIER_PRESENCE:kotlin.String) Carrier presence information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CARRIER_PRESENCE_VT_CAPABLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#CARRIER_PRESENCE_VT_CAPABLE:kotlin.Int) Indicates that the entry is Video Telephony (VT) capable on the current carrier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA1](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA1:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA10](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA10:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA11](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA11:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA12](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA12:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA13](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA13:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA14](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA14:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA15](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA15:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA2](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA2:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA3](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA3:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA4](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA4:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA5](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA5:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA6](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA6:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA7](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA7:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA8](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA8:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA9](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA9:kotlin.String) Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA_VERSION](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#DATA_VERSION:kotlin.String) The version of this data record. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_PRIMARY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#IS_PRIMARY:kotlin.String) Whether this is the primary entry of its kind for the raw contact it belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_READ_ONLY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#IS_READ_ONLY:kotlin.String) The "read-only" flag: "0" by default, "1" if the row cannot be modified or deleted except by a sync adapter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_SUPER_PRIMARY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#IS_SUPER_PRIMARY:kotlin.String) Whether this is the primary entry of its kind for the aggregate contact it belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) The MIME type of the item represented by this row. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PREFERRED_PHONE_ACCOUNT_COMPONENT_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#PREFERRED_PHONE_ACCOUNT_COMPONENT_NAME:kotlin.String) The flattened [android.content.ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) of a that is the preferred`PhoneAccountHandle`to call the contact with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PREFERRED_PHONE_ACCOUNT_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#PREFERRED_PHONE_ACCOUNT_ID:kotlin.String) The ID of a that is the preferred`PhoneAccountHandle`to call the contact with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RAW_CONTACT_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#RAW_CONTACT_ID:kotlin.String) A reference to the [RawContacts._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) that this data belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RES_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#RES_PACKAGE:kotlin.String) The package name to use when creating [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) objects for this data row. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC1](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#SYNC1:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC2](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#SYNC2:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC3](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#SYNC3:kotlin.String) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC4](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#SYNC4:kotlin.String) Generic column for use by sync adapters. |

## Constants

### CARRIER_PRESENCE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CARRIER_PRESENCE: String
```

**Deprecated:** *The contacts database will only show presence information on devices where [android.telephony.CarrierConfigManager#KEY_USE_RCS_PRESENCE_BOOL](https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_USE_RCS_PRESENCE_BOOL:kotlin.String) is true, otherwise use [android.telephony.ims.RcsUceAdapter](https://developer.android.com/reference/kotlin/android/telephony/ims/RcsUceAdapter.html#).*

Carrier presence information.

Type: INTEGER (A bitmask of CARRIER_PRESENCE_\* fields) 

 Value: "carrier_presence"

### CARRIER_PRESENCE_VT_CAPABLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CARRIER_PRESENCE_VT_CAPABLE: Int
```

**Deprecated:** *Same as [DataColumns.CARRIER_PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#CARRIER_PRESENCE:kotlin.String).*

Indicates that the entry is Video Telephony (VT) capable on the current carrier. An allowed bitmask of [CARRIER_PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#CARRIER_PRESENCE:kotlin.String). 

 Value: 1

### DATA1

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA1: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data1"

### DATA10

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA10: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data10"

### DATA11

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA11: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data11"

### DATA12

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA12: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data12"

### DATA13

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA13: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data13"

### DATA14

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA14: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data14"

### DATA15

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA15: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific. By convention, this field is used to store BLOBs (binary data). 

 Value: "data15"

### DATA2

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA2: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data2"

### DATA3

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA3: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data3"

### DATA4

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA4: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data4"

### DATA5

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA5: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data5"

### DATA6

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA6: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data6"

### DATA7

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA7: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data7"

### DATA8

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA8: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data8"

### DATA9

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA9: String
```

Generic data column, the meaning is [MIMETYPE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#MIMETYPE:kotlin.String) specific 

 Value: "data9"

### DATA_VERSION

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_VERSION: String
```

The version of this data record. This is a read-only value. The data column is guaranteed to not change without the version going up. This value is monotonically increasing.

Type: INTEGER 

 Value: "data_version"

### IS_PRIMARY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_PRIMARY: String
```

Whether this is the primary entry of its kind for the raw contact it belongs to.

Type: INTEGER (if set, non-0 means true) 

 Value: "is_primary"

### IS_READ_ONLY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_READ_ONLY: String
```

The "read-only" flag: "0" by default, "1" if the row cannot be modified or deleted except by a sync adapter. See [ContactsContract.CALLER_IS_SYNCADAPTER](https://developer.android.com/reference/kotlin/android/provider/ContactsContract#CALLER_IS_SYNCADAPTER:kotlin.String).

Type: INTEGER 

 Value: "is_read_only"

### IS_SUPER_PRIMARY

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IS_SUPER_PRIMARY: String
```

Whether this is the primary entry of its kind for the aggregate contact it belongs to. Any data record that is "super primary" must also be "primary".

Type: INTEGER (if set, non-0 means true) 

 Value: "is_super_primary"

### MIMETYPE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MIMETYPE: String
```

The MIME type of the item represented by this row. 

 Value: "mimetype"

### PREFERRED_PHONE_ACCOUNT_COMPONENT_NAME

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREFERRED_PHONE_ACCOUNT_COMPONENT_NAME: String
```

The flattened [android.content.ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) of a that is the preferred`PhoneAccountHandle`to call the contact with.

On a multi-SIM device this field can be used in a [CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) row to indicate the [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#) to call the number with, instead of using [android.telecom.TelecomManager#getDefaultOutgoingPhoneAccount(String)](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#getDefaultOutgoingPhoneAccount(kotlin.String))or asking every time.

[android.telecom.TelecomManager#placeCall(Uri, android.os.Bundle)](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#placeCall(android.net.Uri,%20android.os.Bundle))should be called with [android.telecom.TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String) set to the [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#) using the [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) from this field. 

 Value: "preferred_phone_account_component_name"

**See Also**

- [#PREFERRED_PHONE_ACCOUNT_ID](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#PREFERRED_PHONE_ACCOUNT_ID:kotlin.String)
- [android.telecom.PhoneAccountHandle#getComponentName()](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#getComponentName())
- [android.content.ComponentName#flattenToString()](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#flattenToString()) 

### PREFERRED_PHONE_ACCOUNT_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREFERRED_PHONE_ACCOUNT_ID: String
```

The ID of a that is the preferred`PhoneAccountHandle`to call the contact with. Used by [CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone).

On a multi-SIM device this field can be used in a [CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) row to indicate the [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#) to call the number with, instead of using [android.telecom.TelecomManager#getDefaultOutgoingPhoneAccount(String)](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#getDefaultOutgoingPhoneAccount(kotlin.String))or asking every time.

[android.telecom.TelecomManager#placeCall(Uri, android.os.Bundle)](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#placeCall(android.net.Uri,%20android.os.Bundle))should be called with [android.telecom.TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE](https://developer.android.com/reference/kotlin/android/telecom/TelecomManager.html#EXTRA_PHONE_ACCOUNT_HANDLE:kotlin.String) set to the [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#) using the id from this field. 

 Value: "preferred_phone_account_id"

**See Also**

- [#PREFERRED_PHONE_ACCOUNT_COMPONENT_NAME](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumns#PREFERRED_PHONE_ACCOUNT_COMPONENT_NAME:kotlin.String)
- [android.telecom.PhoneAccountHandle#getId()](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#getId()) 

### RAW_CONTACT_ID

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_CONTACT_ID: String
```

A reference to the [RawContacts._ID](https://developer.android.com/reference/kotlin/android/provider/BaseColumns#_ID:kotlin.String) that this data belongs to. 

 Value: "raw_contact_id"

### RES_PACKAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RES_PACKAGE: String
```

The package name to use when creating [Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) objects for this data row. This value is only designed for use when building user interfaces, and should not be used to infer the owner. 

 Value: "res_package"

### SYNC1

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC1: String
```

Generic column for use by sync adapters. 

 Value: "data_sync1"

### SYNC2

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC2: String
```

Generic column for use by sync adapters. 

 Value: "data_sync2"

### SYNC3

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC3: String
```

Generic column for use by sync adapters. 

 Value: "data_sync3"

### SYNC4

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYNC4: String
```

Generic column for use by sync adapters. 

 Value: "data_sync4"
