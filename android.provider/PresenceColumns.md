# Contacts.PresenceColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PresenceColumns

Kotlin| [Java](../android/provider/Contacts.PresenceColumns.md) 
| --- | --- |

```
interface PresenceColumns
```

| [android.provider.Contacts.PresenceColumns](../android/provider/Contacts.PresenceColumns.md) |

| Known Direct Subclasses [Contacts.People](../android/provider/Contacts.People.md) |----------------------------------------------------------------------------------------------------|-----------------------------| | [Contacts.People](../android/provider/Contacts.People.md) | This table contains people. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](../android/provider/ContactsContract.md)

The IM presence columns with some contacts specific columns mixed in.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AVAILABLE](../android/provider/Contacts.PresenceColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [AWAY](../android/provider/Contacts.PresenceColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DO_NOT_DISTURB](../android/provider/Contacts.PresenceColumns.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [IDLE](../android/provider/Contacts.PresenceColumns.md) <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IM_ACCOUNT](../android/provider/Contacts.PresenceColumns.md) The IM account for the local user that the presence data came from. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IM_HANDLE](../android/provider/Contacts.PresenceColumns.md) The IM handle the presence item is for. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [IM_PROTOCOL](../android/provider/Contacts.PresenceColumns.md) The IM service the presence is coming from. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVISIBLE](../android/provider/Contacts.PresenceColumns.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OFFLINE](../android/provider/Contacts.PresenceColumns.md) Presence Status definition |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE_CUSTOM_STATUS](../android/provider/Contacts.PresenceColumns.md) The user defined status line. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRESENCE_STATUS](../android/provider/Contacts.PresenceColumns.md) The server defined status. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PRIORITY](../android/provider/Contacts.PresenceColumns.md) The priority, an integer, used by XMPP presence |
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

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The IM account for the local user that the presence data came from.

Type: STRING 

 Value: "im_account"

### IM_HANDLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IM_HANDLE: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The IM handle the presence item is for. The handle is scoped to the [IM_PROTOCOL](../android/provider/Contacts.PresenceColumns.md).

Type: STRING 

 Value: "im_handle"

### IM_PROTOCOL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val IM_PROTOCOL: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The IM service the presence is coming from. Formatted using either [Contacts.ContactMethods.encodePredefinedImProtocol](../android/provider/Contacts.ContactMethods.md))or [Contacts.ContactMethods.encodeCustomImProtocol](../android/provider/Contacts.ContactMethods.md)).

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
