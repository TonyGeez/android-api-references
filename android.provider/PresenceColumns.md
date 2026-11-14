# Contacts.PresenceColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PresenceColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.PresenceColumns "View this page in Java") 
| --- | --- |

```
interface PresenceColumns
```

| [android.provider.Contacts.PresenceColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#) |

| Known Direct Subclasses [Contacts.People](https://developer.android.com/reference/kotlin/android/provider/Contacts.People) |----------------------------------------------------------------------------------------------------|-----------------------------| | [Contacts.People](https://developer.android.com/reference/kotlin/android/provider/Contacts.People) | This table contains people. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

The IM presence columns with some contacts specific columns mixed in.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABLE](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#AVAILABLE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AWAY](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#AWAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DO_NOT_DISTURB](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#DO_NOT_DISTURB:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDLE](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#IDLE:kotlin.Int) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IM_ACCOUNT](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#IM_ACCOUNT:kotlin.String) The IM account for the local user that the presence data came from. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IM_HANDLE](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#IM_HANDLE:kotlin.String) The IM handle the presence item is for. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IM_PROTOCOL](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#IM_PROTOCOL:kotlin.String) The IM service the presence is coming from. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVISIBLE](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#INVISIBLE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OFFLINE](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#OFFLINE:kotlin.Int) Presence Status definition |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE_CUSTOM_STATUS](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#PRESENCE_CUSTOM_STATUS:kotlin.String) The user defined status line. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE_STATUS](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#PRESENCE_STATUS:kotlin.String) The server defined status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRIORITY](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#PRIORITY:kotlin.String) The priority, an integer, used by XMPP presence |
| --- | --- |

## Constants

### AVAILABLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AVAILABLE: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 5

### AWAY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AWAY: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 2

### DO_NOT_DISTURB

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DO_NOT_DISTURB: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 4

### IDLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IDLE: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 3

### IM_ACCOUNT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IM_ACCOUNT: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The IM account for the local user that the presence data came from.

Type: STRING 

 Value: "im_account"

### IM_HANDLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IM_HANDLE: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The IM handle the presence item is for. The handle is scoped to the [IM_PROTOCOL](https://developer.android.com/reference/kotlin/android/provider/Contacts.PresenceColumns#IM_PROTOCOL:kotlin.String).

Type: STRING 

 Value: "im_handle"

### IM_PROTOCOL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IM_PROTOCOL: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The IM service the presence is coming from. Formatted using either [Contacts.ContactMethods.encodePredefinedImProtocol](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethods#encodePredefinedImProtocol(kotlin.Int))or [Contacts.ContactMethods.encodeCustomImProtocol](https://developer.android.com/reference/kotlin/android/provider/Contacts.ContactMethods#encodeCustomImProtocol(kotlin.String)).

Type: STRING 

 Value: "im_protocol"

### INVISIBLE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVISIBLE: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 1

### OFFLINE

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OFFLINE: Int
```

**Deprecated:** *Deprecated in Java.*

Presence Status definition 

 Value: 0

### PRESENCE_CUSTOM_STATUS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESENCE_CUSTOM_STATUS: String
```

**Deprecated:** *Deprecated in Java.*

The user defined status line.

Type: TEXT 

 Value: "status"

### PRESENCE_STATUS

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESENCE_STATUS: String
```

**Deprecated:** *Deprecated in Java.*

The server defined status.

Type: INTEGER (one of the values below) 

 Value: "mode"

### PRIORITY

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRIORITY: String
```

**Deprecated:** *Deprecated in Java.*

The priority, an integer, used by XMPP presence

Type: INTEGER 

 Value: "priority"
