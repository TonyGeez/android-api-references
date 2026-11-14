# ContactsContract.StatusColumns

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StatusColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/ContactsContract.StatusColumns "View this page in Java") 

```
protected interface StatusColumns
```

| [android.provider.ContactsContract.StatusColumns](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#) |

| Known Direct Subclasses [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity), [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins), [ContactsContract.StatusUpdates](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusUpdates) |------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.Contacts.Entity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Entity) | A sub-directory of a contact that contains all of its [ContactsContract.RawContacts](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.RawContacts) as well as [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) rows. | | [ContactsContract.DataColumnsWithJoins](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.DataColumnsWithJoins) | Combines all columns returned by [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) table queries. | | [ContactsContract.StatusUpdates](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusUpdates) | A status update is linked to a [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) row and captures the user's latest status update via the corresponding source, e. | |

| Known Indirect Subclasses [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable), [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables), [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email), [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event), [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership), [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity), [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im), [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname), [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note), [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization), [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone), [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo), and 8 others. |------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContactsContract.CommonDataKinds.Callable](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Callable) | Convenient functionalities for "callable" data. | | [ContactsContract.CommonDataKinds.Contactables](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Contactables) | A special class of data items, used to refer to types of data that can be used to attempt to start communicating with a person ([Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) and [Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email)). | | [ContactsContract.CommonDataKinds.Email](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Email) | A data kind representing an email address. | | [ContactsContract.CommonDataKinds.Event](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Event) | A data kind representing an event. | | [ContactsContract.CommonDataKinds.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.GroupMembership) | Group Membership. | | [ContactsContract.CommonDataKinds.Identity](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Identity) | A data kind representing an Identity related to the contact. | | [ContactsContract.CommonDataKinds.Im](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Im) | A data kind representing an IM address | | [ContactsContract.CommonDataKinds.Nickname](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Nickname) | A data kind representing the contact's nickname. | | [ContactsContract.CommonDataKinds.Note](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Note) | Notes about the contact. | | [ContactsContract.CommonDataKinds.Organization](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Organization) | A data kind representing an organization. | | [ContactsContract.CommonDataKinds.Phone](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Phone) | A data kind representing a telephone number. | | [ContactsContract.CommonDataKinds.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Photo) | A data kind representing a photo for the contact. | | [ContactsContract.CommonDataKinds.Relation](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Relation) | A data kind representing a relation. | | [ContactsContract.CommonDataKinds.SipAddress](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.SipAddress) | A data kind representing a SIP address for the contact. | | [ContactsContract.CommonDataKinds.StructuredName](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredName) | A data kind representing the contact's proper name. | | [ContactsContract.CommonDataKinds.StructuredPostal](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.StructuredPostal) | A data kind representing a postal addresses. | | [ContactsContract.CommonDataKinds.Website](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.CommonDataKinds.Website) | A data kind representing a website related to the contact. | | [ContactsContract.Contacts.Photo](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Contacts.Photo) | A*read-only*sub-directory of a single contact that contains the contact's primary photo. | | [ContactsContract.Data](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Data) | Constants for the data table, which contains data points tied to a raw contact. | | [ContactsContract.Presence](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.Presence) | <br /> | |

Social status update columns.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#AVAILABLE:kotlin.Int) An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AWAY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#AWAY:kotlin.Int) An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_HAS_CAMERA](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CAPABILITY_HAS_CAMERA:kotlin.Int) An allowed flag of [CHAT_CAPABILITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CHAT_CAPABILITY:kotlin.String). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_HAS_VIDEO](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CAPABILITY_HAS_VIDEO:kotlin.Int) An allowed flag of [CHAT_CAPABILITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CHAT_CAPABILITY:kotlin.String). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CAPABILITY_HAS_VOICE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CAPABILITY_HAS_VOICE:kotlin.Int) An allowed flag of [CHAT_CAPABILITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CHAT_CAPABILITY:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CHAT_CAPABILITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CHAT_CAPABILITY:kotlin.String) Contact's audio/video chat capability level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DO_NOT_DISTURB](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#DO_NOT_DISTURB:kotlin.Int) An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#IDLE:kotlin.Int) An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVISIBLE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#INVISIBLE:kotlin.Int) An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OFFLINE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#OFFLINE:kotlin.Int) An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String) Contact's latest presence level. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE_CUSTOM_STATUS](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE_CUSTOM_STATUS:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE_STATUS](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE_STATUS:kotlin.String) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#STATUS:kotlin.String) Contact latest status update. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS_ICON](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#STATUS_ICON:kotlin.String) The resource ID of the icon for the source of the status update. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS_LABEL](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#STATUS_LABEL:kotlin.String) The resource ID of the label describing the source of the status update, e. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS_RES_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#STATUS_RES_PACKAGE:kotlin.String) The package containing resources for this status: label and icon. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STATUS_TIMESTAMP](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#STATUS_TIMESTAMP:kotlin.String) The absolute time in milliseconds when the latest status was inserted/updated. |

## Constants

### AVAILABLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABLE: Int
```

An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). 

 Value: 5

### AWAY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AWAY: Int
```

An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). 

 Value: 2

### CAPABILITY_HAS_CAMERA

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_HAS_CAMERA: Int
```

An allowed flag of [CHAT_CAPABILITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CHAT_CAPABILITY:kotlin.String). Indicates that the contact's device has a camera that can be used for video chat (e.g. a front-facing camera on a phone). 

 Value: 4

### CAPABILITY_HAS_VIDEO

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_HAS_VIDEO: Int
```

An allowed flag of [CHAT_CAPABILITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CHAT_CAPABILITY:kotlin.String). Indicates that the contact's device can display a video feed. 

 Value: 2

### CAPABILITY_HAS_VOICE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CAPABILITY_HAS_VOICE: Int
```

An allowed flag of [CHAT_CAPABILITY](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#CHAT_CAPABILITY:kotlin.String). Indicates audio-chat capability (microphone and speaker) 

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

An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). 

 Value: 4

### IDLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDLE: Int
```

An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). 

 Value: 3

### INVISIBLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVISIBLE: Int
```

An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). 

 Value: 1

### OFFLINE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OFFLINE: Int
```

An allowed value of [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String). 

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

**Deprecated:** *use [STATUS](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#STATUS:kotlin.String)* 

 Value: "status"

### PRESENCE_STATUS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESENCE_STATUS: String
```

**Deprecated:** *use [PRESENCE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#PRESENCE:kotlin.String)* 

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

The resource ID of the icon for the source of the status update. This resource should be scoped by the [STATUS_RES_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#STATUS_RES_PACKAGE:kotlin.String).

Type: NUMBER 

 Value: "status_icon"

### STATUS_LABEL

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_LABEL: String
```

The resource ID of the label describing the source of the status update, e.g. "Google Talk". This resource should be scoped by the [STATUS_RES_PACKAGE](https://developer.android.com/reference/kotlin/android/provider/ContactsContract.StatusColumns#STATUS_RES_PACKAGE:kotlin.String).

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
