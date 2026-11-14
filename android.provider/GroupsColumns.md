# Contacts.GroupsColumns

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GroupsColumns

Kotlin| [Java](../android/provider/Contacts.GroupsColumns.md) 
| --- | --- |

```
interface GroupsColumns
```

| [android.provider.Contacts.GroupsColumns](../android/provider/Contacts.GroupsColumns.md) |

| Known Direct Subclasses [Contacts.GroupMembership](../android/provider/Contacts.GroupMembership.md), [Contacts.Groups](../android/provider/Contacts.Groups.md) |----------------------------------------------------------------------------------------------------------------------|------------------------------------------------| | [Contacts.GroupMembership](../android/provider/Contacts.GroupMembership.md) | <br /> | | [Contacts.Groups](../android/provider/Contacts.Groups.md) | This table contains the groups for an account. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 5.**
|
| see [android.provider.ContactsContract](../android/provider/ContactsContract.md)

Columns from the groups table.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NAME](../android/provider/Contacts.GroupsColumns.md) The group name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [NOTES](../android/provider/Contacts.GroupsColumns.md) Notes about the group. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SHOULD_SYNC](../android/provider/Contacts.GroupsColumns.md) Whether this group should be synced if the SYNC_EVERYTHING settings is false for this group's account. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SYSTEM_ID](../android/provider/Contacts.GroupsColumns.md) The ID of this group if it is a System Group, null otherwise. |

## Constants

### NAME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NAME: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The group name.

Type: TEXT 

 Value: "name"

### NOTES

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NOTES: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Notes about the group.

Type: TEXT 

 Value: "notes"

### SHOULD_SYNC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOULD_SYNC: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

Whether this group should be synced if the SYNC_EVERYTHING settings is false for this group's account.

Type: INTEGER (boolean) 

 Value: "should_sync"

### SYSTEM_ID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SYSTEM_ID: String
```

**Deprecated:** *see [android.provider.ContactsContract](../android/provider/ContactsContract.md)*

The ID of this group if it is a System Group, null otherwise.

Type: TEXT 

 Value: "system_id"
