# Contacts.GroupsColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GroupsColumns

Kotlin| [Java](https://developer.android.com/reference/android/provider/Contacts.GroupsColumns "View this page in Java") 

```
interface GroupsColumns
```

| [android.provider.Contacts.GroupsColumns](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupsColumns#) |

| Known Direct Subclasses [Contacts.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupMembership), [Contacts.Groups](https://developer.android.com/reference/kotlin/android/provider/Contacts.Groups) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------| | [Contacts.GroupMembership](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupMembership) | <br /> | | [Contacts.Groups](https://developer.android.com/reference/kotlin/android/provider/Contacts.Groups) | This table contains the groups for an account. | |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)

Columns from the groups table.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupsColumns#NAME:kotlin.String) The group name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NOTES](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupsColumns#NOTES:kotlin.String) Notes about the group. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SHOULD_SYNC](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupsColumns#SHOULD_SYNC:kotlin.String) Whether this group should be synced if the SYNC_EVERYTHING settings is false for this group's account. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYSTEM_ID](https://developer.android.com/reference/kotlin/android/provider/Contacts.GroupsColumns#SYSTEM_ID:kotlin.String) The ID of this group if it is a System Group, null otherwise. |

## Constants

### NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The group name.

Type: TEXT 

 Value: "name"

### NOTES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTES: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Notes about the group.

Type: TEXT 

 Value: "notes"

### SHOULD_SYNC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOULD_SYNC: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

Whether this group should be synced if the SYNC_EVERYTHING settings is false for this group's account.

Type: INTEGER (boolean) 

 Value: "should_sync"

### SYSTEM_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYSTEM_ID: String
```

**Deprecated:** *see [android.provider.ContactsContract](https://developer.android.com/reference/kotlin/android/provider/ContactsContract)*

The ID of this group if it is a System Group, null otherwise.

Type: TEXT 

 Value: "system_id"
