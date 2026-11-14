# ContactsContract.StatusColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatusColumns

Kotlin| [Java](../android/provider/ContactsContract.StatusColumns.md) 
| --- | --- |

```
protected interface StatusColumns
```

| [android.provider.ContactsContract.StatusColumns](../android/provider/ContactsContract.StatusColumns.md) |

| Known Direct Subclasses [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md), [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md), [ContactsContract.StatusUpdates](../android/provider/ContactsContract.StatusUpdates.md) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](../android/provider/ContactsContract.Contacts.Entity.md) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](../android/provider/ContactsContract.RawContacts.md) as well as [ContactsContract.Data](../android/provider/ContactsContract.Data.md) rows. | | [ContactsContract.DataColumnsWithJoins](../android/provider/ContactsContract.DataColumnsWithJoins.md) | Combines all columns returned by [ContactsContract.Data](../android/provider/ContactsContract.Data.md) table queries. | | [ContactsContract.StatusUpdates](../android/provider/ContactsContract.StatusUpdates.md) | A status update is linked to a [ContactsContract.Data](../android/provider/ContactsContract.Data.md) row and captures the user's latest status update via the corresponding source, e. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md), [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md), [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md), [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md), [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md), [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md), [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md), [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md), [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md), [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md), [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md), [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md), and 8 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](../android/provider/ContactsContract.CommonDataKinds.Callable.md) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](../android/provider/ContactsContract.CommonDataKinds.Contactables.md) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) and [Email](../android/provider/ContactsContract.CommonDataKinds.Email.md)). | | [ContactsContract.CommonDataKinds.Email](../android/provider/ContactsContract.CommonDataKinds.Email.md) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](../android/provider/ContactsContract.CommonDataKinds.Event.md) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](../android/provider/ContactsContract.CommonDataKinds.GroupMembership.md) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](../android/provider/ContactsContract.CommonDataKinds.Identity.md) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](../android/provider/ContactsContract.CommonDataKinds.Im.md) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](../android/provider/ContactsContract.CommonDataKinds.Nickname.md) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](../android/provider/ContactsContract.CommonDataKinds.Note.md) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](../android/provider/ContactsContract.CommonDataKinds.Organization.md) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](../android/provider/ContactsContract.CommonDataKinds.Phone.md) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](../android/provider/ContactsContract.CommonDataKinds.Photo.md) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](../android/provider/ContactsContract.CommonDataKinds.Relation.md) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](../android/provider/ContactsContract.CommonDataKinds.SipAddress.md) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](../android/provider/ContactsContract.CommonDataKinds.StructuredName.md) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](../android/provider/ContactsContract.CommonDataKinds.StructuredPostal.md) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](../android/provider/ContactsContract.CommonDataKinds.Website.md) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](../android/provider/ContactsContract.Contacts.Photo.md) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](../android/provider/ContactsContract.Data.md) | Constants for the data table, which contains data points tied to a raw contact. | | [ContactsContract.Presence](../android/provider/ContactsContract.Presence.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Social status update columns.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABLE](../android/provider/ContactsContract.StatusColumns.md) An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AWAY](../android/provider/ContactsContract.StatusColumns.md) An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_HAS_CAMERA](../android/provider/ContactsContract.StatusColumns.md) An allowed flag of [CHAT_CAPABILITY](../android/provider/ContactsContract.StatusColumns.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_HAS_VIDEO](../android/provider/ContactsContract.StatusColumns.md) An allowed flag of [CHAT_CAPABILITY](../android/provider/ContactsContract.StatusColumns.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_HAS_VOICE](../android/provider/ContactsContract.StatusColumns.md) An allowed flag of [CHAT_CAPABILITY](../android/provider/ContactsContract.StatusColumns.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHAT_CAPABILITY](../android/provider/ContactsContract.StatusColumns.md) Contact's audio/video chat capability level. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DO_NOT_DISTURB](../android/provider/ContactsContract.StatusColumns.md) An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDLE](../android/provider/ContactsContract.StatusColumns.md) An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVISIBLE](../android/provider/ContactsContract.StatusColumns.md) An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OFFLINE](../android/provider/ContactsContract.StatusColumns.md) An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE](../android/provider/ContactsContract.StatusColumns.md) Contact's latest presence level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE_CUSTOM_STATUS](../android/provider/ContactsContract.StatusColumns.md) <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE_STATUS](../android/provider/ContactsContract.StatusColumns.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS](../android/provider/ContactsContract.StatusColumns.md) Contact latest status update. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS_ICON](../android/provider/ContactsContract.StatusColumns.md) The resource ID of the icon for the source of the status update. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS_LABEL](../android/provider/ContactsContract.StatusColumns.md) The resource ID of the label describing the source of the status update, e. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS_RES_PACKAGE](../android/provider/ContactsContract.StatusColumns.md) The package containing resources for this status: label and icon. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS_TIMESTAMP](../android/provider/ContactsContract.StatusColumns.md) The absolute time in milliseconds when the latest status was inserted/updated. |
| --- | --- |

## Constants

### AVAILABLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABLE: Int
```

An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). 

 Value: 5

### AWAY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AWAY: Int
```

An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). 

 Value: 2

### CAPABILITY_HAS_CAMERA

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_HAS_CAMERA: Int
```

An allowed flag of [CHAT_CAPABILITY](../android/provider/ContactsContract.StatusColumns.md). Indicates that the contact's device has a camera that can be used for video chat (e.g. a front-facing camera on a phone). 

 Value: 4

### CAPABILITY_HAS_VIDEO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_HAS_VIDEO: Int
```

An allowed flag of [CHAT_CAPABILITY](../android/provider/ContactsContract.StatusColumns.md). Indicates that the contact's device can display a video feed. 

 Value: 2

### CAPABILITY_HAS_VOICE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_HAS_VOICE: Int
```

An allowed flag of [CHAT_CAPABILITY](../android/provider/ContactsContract.StatusColumns.md). Indicates audio-chat capability (microphone and speaker) 

 Value: 1

### CHAT_CAPABILITY

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHAT_CAPABILITY: String
```

Contact's audio/video chat capability level.

Type: INTEGER (one of the values below) 

 Value: "chat_capability"

### DO_NOT_DISTURB

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DO_NOT_DISTURB: Int
```

An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). 

 Value: 4

### IDLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDLE: Int
```

An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). 

 Value: 3

### INVISIBLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVISIBLE: Int
```

An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). 

 Value: 1

### OFFLINE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OFFLINE: Int
```

An allowed value of [PRESENCE](../android/provider/ContactsContract.StatusColumns.md). 

 Value: 0

### PRESENCE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESENCE: String
```

Contact's latest presence level.

Type: INTEGER (one of the values below) 

 Value: "mode"

### PRESENCE_CUSTOM_STATUS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESENCE_CUSTOM_STATUS: String
```

**Deprecated:** *use [STATUS](../android/provider/ContactsContract.StatusColumns.md)* 

 Value: "status"

### PRESENCE_STATUS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESENCE_STATUS: String
```

**Deprecated:** *use [PRESENCE](../android/provider/ContactsContract.StatusColumns.md)* 

 Value: "mode"

### STATUS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS: String
```

Contact latest status update.

Type: TEXT 

 Value: "status"

### STATUS_ICON

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ICON: String
```

The resource ID of the icon for the source of the status update. This resource should be scoped by the [STATUS_RES_PACKAGE](../android/provider/ContactsContract.StatusColumns.md).

Type: NUMBER 

 Value: "status_icon"

### STATUS_LABEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_LABEL: String
```

The resource ID of the label describing the source of the status update, e.g. "Google Talk". This resource should be scoped by the [STATUS_RES_PACKAGE](../android/provider/ContactsContract.StatusColumns.md).

Type: NUMBER 

 Value: "status_label"

### STATUS_RES_PACKAGE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_RES_PACKAGE: String
```

The package containing resources for this status: label and icon.

Type: TEXT 

 Value: "status_res_package"

### STATUS_TIMESTAMP

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_TIMESTAMP: String
```

The absolute time in milliseconds when the latest status was inserted/updated.

Type: NUMBER 

 Value: "status_ts"
