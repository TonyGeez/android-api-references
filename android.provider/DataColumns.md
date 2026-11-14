# ContactsContract.DataColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataColumns

Kotlin| [Java](../android/provider/ContactsContract.DataColumns.md) 
| --- | --- |

```
protected interface DataColumns
```

| [android.provider.ContactsContract.DataColumns](../android/provider/ContactsContract.DataColumns.md) |

| Known Direct Subclasses [ContactsContract.Contacts.Data](../android/provider/ContactsContract.Contacts.Data.md), [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md), [ContactsContract.RawContacts.Data](../android/provider/ContactsContract.RawContacts.Data.md), [ContactsContract.RawContacts.Entity](../android/provider/ContactsContract.RawContacts.Entity.md), [ContactsContract.RawContactsEntity](../android/provider/ContactsContract.RawContactsEntity.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Data](../android/provider/ContactsContract.Contacts.Data.md) | A sub-directory of a single contact that contains all of the constituent raw contact [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) | Combines all columns returned by [ContactsContract.Data](../android/provider/ContactsContract.Data.md) table queries. | | [ContactsContract.RawContacts.Data](../android/provider/ContactsContract.RawContacts.Data.md) | A sub-directory of a single raw contact that contains all of its [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.RawContacts.Entity](../android/provider/ContactsContract.RawContacts.Entity.md) | A sub-directory of a single raw contact that contains all of its [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.RawContactsEntity](../android/provider/ContactsContract.RawContactsEntity.md) | Constants for the raw contacts entities table, which can be thought of as an outer join of the raw_contacts table with the data table. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md), [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md), [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md), [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md), [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md), [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md), [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md), [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md), [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md), [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md), [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md), [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) and [Email](../android/provider/ContactsContract.CommonDataKinds.Email.md)). | | [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](../android/provider/ContactsContract.CommonDataKinds.Relation.md) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](../android/provider/ContactsContract.CommonDataKinds.SipAddress.md) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](../android/provider/ContactsContract.CommonDataKinds.StructuredName.md) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](../android/provider/ContactsContract.CommonDataKinds.StructuredPostal.md) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](../android/provider/ContactsContract.CommonDataKinds.Website.md) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](../android/provider/ContactsContract.Contacts.Photo.md) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](../android/provider/ContactsContract.Data.md) | Constants for the data table, which contains data points tied to a raw contact. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Columns in the Data table.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CARRIER_PRESENCE](../android/provider/ContactsContract.DataColumns.md) Carrier presence information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CARRIER_PRESENCE_VT_CAPABLE](../android/provider/ContactsContract.DataColumns.md) Indicates that the entry is Video Telephony (VT) capable on the current carrier. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA1](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA10](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA11](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA12](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA13](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA14](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA15](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA2](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA3](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA4](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA5](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA6](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA7](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA8](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA9](../android/provider/ContactsContract.DataColumns.md) Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DATA_VERSION](../android/provider/ContactsContract.DataColumns.md) The version of this data record. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_PRIMARY](../android/provider/ContactsContract.DataColumns.md) Whether this is the primary entry of its kind for the raw contact it belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_READ_ONLY](../android/provider/ContactsContract.DataColumns.md) The "read-only" flag: "0" by default, "1" if the row cannot be modified or deleted except by a sync adapter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IS_SUPER_PRIMARY](../android/provider/ContactsContract.DataColumns.md) Whether this is the primary entry of its kind for the aggregate contact it belongs to. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) The MIME type of the item represented by this row. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PREFERRED_PHONE_ACCOUNT_COMPONENT_NAME](../android/provider/ContactsContract.DataColumns.md) The flattened [android.content.ComponentName](../android.content/ComponentName.md) of a that is the preferred`PhoneAccountHandle`to call the contact with. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PREFERRED_PHONE_ACCOUNT_ID](../android/provider/ContactsContract.DataColumns.md) The ID of a that is the preferred`PhoneAccountHandle`to call the contact with. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RAW_CONTACT_ID](../android/provider/ContactsContract.DataColumns.md) A reference to the [RawContacts._ID](BaseColumns.md) that this data belongs to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [RES_PACKAGE](../android/provider/ContactsContract.DataColumns.md) The package name to use when creating [Resources](../android.content.res/Resources.md) objects for this data row. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC1](../android/provider/ContactsContract.DataColumns.md) Generic column for use by sync adapters. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC2](../android/provider/ContactsContract.DataColumns.md) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC3](../android/provider/ContactsContract.DataColumns.md) Generic column for use by sync adapters. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYNC4](../android/provider/ContactsContract.DataColumns.md) Generic column for use by sync adapters. |
| --- | --- |

## Constants

### CARRIER_PRESENCE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CARRIER_PRESENCE: String
```

**Deprecated:** *The contacts database will only show presence information on devices where [android.telephony.CarrierConfigManager#KEY_USE_RCS_PRESENCE_BOOL](../android.telephony/CarrierConfigManager.md) is true, otherwise use [android.telephony.ims.RcsUceAdapter](../android.telephony.ims/RcsUceAdapter.md).*

Carrier presence information.

Type: INTEGER (A bitmask of CARRIER_PRESENCE_\* fields) 

 Value: "carrier_presence"

### CARRIER_PRESENCE_VT_CAPABLE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CARRIER_PRESENCE_VT_CAPABLE: Int
```

**Deprecated:** *Same as [DataColumns.CARRIER_PRESENCE](../android/provider/ContactsContract.DataColumns.md).*

Indicates that the entry is Video Telephony (VT) capable on the current carrier. An allowed bitmask of [CARRIER_PRESENCE](../android/provider/ContactsContract.DataColumns.md). 

 Value: 1

### DATA1

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA1: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data1"

### DATA10

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA10: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data10"

### DATA11

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA11: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data11"

### DATA12

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA12: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data12"

### DATA13

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA13: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data13"

### DATA14

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA14: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data14"

### DATA15

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA15: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific. By convention, this field is used to store BLOBs (binary data). 

 Value: "data15"

### DATA2

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA2: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data2"

### DATA3

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA3: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data3"

### DATA4

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA4: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data4"

### DATA5

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA5: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data5"

### DATA6

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA6: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data6"

### DATA7

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA7: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data7"

### DATA8

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA8: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

 Value: "data8"

### DATA9

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA9: String
```

Generic data column, the meaning is [MIMETYPE](../android/provider/ContactsContract.DataColumns.md) specific 

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

The "read-only" flag: "0" by default, "1" if the row cannot be modified or deleted except by a sync adapter. See [ContactsContract.CALLER_IS_SYNCADAPTER](ContactsContract.md).

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

The flattened [android.content.ComponentName](../android.content/ComponentName.md) of a that is the preferred`PhoneAccountHandle`to call the contact with.

On a multi-SIM device this field can be used in a [CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) row to indicate the [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md) to call the number with, instead of using [android.telecom.TelecomManager#getDefaultOutgoingPhoneAccount(String)](../android.telecom/TelecomManager.md))or asking every time.

[android.telecom.TelecomManager#placeCall(Uri, android.os.Bundle)](../android.telecom/TelecomManager.md))should be called with [android.telecom.TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE](../android.telecom/TelecomManager.md) set to the [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md) using the [ComponentName](../android.content/ComponentName.md) from this field. 

 Value: "preferred_phone_account_component_name"

**See Also**

- [#PREFERRED_PHONE_ACCOUNT_ID](../android/provider/ContactsContract.DataColumns.md)
- [android.telecom.PhoneAccountHandle#getComponentName()](../android.telecom/PhoneAccountHandle.md))
- [android.content.ComponentName#flattenToString()](../android.content/ComponentName.md)) 

### PREFERRED_PHONE_ACCOUNT_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREFERRED_PHONE_ACCOUNT_ID: String
```

The ID of a that is the preferred`PhoneAccountHandle`to call the contact with. Used by [CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md).

On a multi-SIM device this field can be used in a [CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) row to indicate the [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md) to call the number with, instead of using [android.telecom.TelecomManager#getDefaultOutgoingPhoneAccount(String)](../android.telecom/TelecomManager.md))or asking every time.

[android.telecom.TelecomManager#placeCall(Uri, android.os.Bundle)](../android.telecom/TelecomManager.md))should be called with [android.telecom.TelecomManager#EXTRA_PHONE_ACCOUNT_HANDLE](../android.telecom/TelecomManager.md) set to the [PhoneAccountHandle](../android.telecom/PhoneAccountHandle.md) using the id from this field. 

 Value: "preferred_phone_account_id"

**See Also**

- [#PREFERRED_PHONE_ACCOUNT_COMPONENT_NAME](../android/provider/ContactsContract.DataColumns.md)
- [android.telecom.PhoneAccountHandle#getId()](../android.telecom/PhoneAccountHandle.md)) 

### RAW_CONTACT_ID

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RAW_CONTACT_ID: String
```

A reference to the [RawContacts._ID](BaseColumns.md) that this data belongs to. 

 Value: "raw_contact_id"

### RES_PACKAGE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RES_PACKAGE: String
```

The package name to use when creating [Resources](../android.content.res/Resources.md) objects for this data row. This value is only designed for use when building user interfaces, and should not be used to infer the owner. 

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
