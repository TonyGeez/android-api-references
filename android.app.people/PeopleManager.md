# PeopleManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PeopleManager

Kotlin| [Java](PeopleManager.md) 
| --- | --- |

```
class PeopleManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.people.PeopleManager](PeopleManager.md) |

This class allows interaction with conversation and people data. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOrUpdateStatus](PeopleManager.md))`(`conversationId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `status:` ` [ConversationStatus](ConversationStatus.md)`)` Sets or updates a [ConversationStatus](ConversationStatus.md) for a conversation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearStatus](PeopleManager.md))`(`conversationId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `statusId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Unpublishes a given status from the given conversation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearStatuses](PeopleManager.md))`(`conversationId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Removes all published statuses for the given conversation. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ConversationStatus](ConversationStatus.md)!\> | [getStatuses](PeopleManager.md))`(`conversationId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Returns all of the currently published statuses for a given conversation. |

## Public methods

### addOrUpdateStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addOrUpdateStatus(
    conversationId: String, 
    status: ConversationStatus
): Unit
```

Sets or updates a [ConversationStatus](ConversationStatus.md) for a conversation.

Statuses are meant to represent current information about the conversation. Like notifications, they are transient and are not persisted beyond a reboot, nor are they backed up and restored.

If the provided conversation shortcut is not already pinned, or cached by the system, it will remain cached as long as the status is active.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `conversationId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the [id](../android.content.pm/ShortcutInfo.md))of the shortcut backing the conversation that has an active status This value cannot be`null`. |
| `status` | [ConversationStatus](ConversationStatus.md):the current status for the given conversation This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | whether the role is available in the system |

### clearStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearStatus(
    conversationId: String, 
    statusId: String
): Unit
```

Unpublishes a given status from the given conversation.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `conversationId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the [id](../android.content.pm/ShortcutInfo.md))of the shortcut backing the conversation that has an active status This value cannot be`null`. |
| `statusId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the [id](ConversationStatus.md))of a published status for the given conversation This value cannot be`null`. |

### clearStatuses

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearStatuses(conversationId: String): Unit
```

Removes all published statuses for the given conversation.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `conversationId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the [id](../android.content.pm/ShortcutInfo.md))of the shortcut backing the conversation that has one or more active statuses This value cannot be`null`. |

### getStatuses

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatuses(conversationId: String): MutableList<ConversationStatus!>
```

Returns all of the currently published statuses for a given conversation.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `conversationId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the [id](../android.content.pm/ShortcutInfo.md))of the shortcut backing the conversation that has one or more active statuses This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ConversationStatus](ConversationStatus.md)!> | This value cannot be`null`. |
