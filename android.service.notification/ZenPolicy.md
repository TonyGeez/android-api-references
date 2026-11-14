# ZenPolicy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZenPolicy

Kotlin| [Java](../android/service/notification/ZenPolicy.md) 
| --- | --- |

```
class ZenPolicy : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.notification.ZenPolicy](../android/service/notification/ZenPolicy.md) |

ZenPolicy determines whether to allow certain notifications and their corresponding sounds to play when a device is in Do Not Disturb mode. ZenPolicy also dictates the visual effects of notifications that are intercepted when a device is in Do Not Disturb mode.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/notification/ZenPolicy.Builder.md) Builder class for [ZenPolicy](../android/service/notification/ZenPolicy.md) objects. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_ANYONE](../android/service/notification/ZenPolicy.md) Used to indicate all conversations can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_IMPORTANT](../android/service/notification/ZenPolicy.md) Used to indicate important conversations can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_NONE](../android/service/notification/ZenPolicy.md) Used to indicate no conversations can bypass dnd. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_UNSET](../android/service/notification/ZenPolicy.md) Used to indicate no preference for the type of conversations that can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_ANYONE](../android/service/notification/ZenPolicy.md) Used to indicate all calls or messages can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_CONTACTS](../android/service/notification/ZenPolicy.md) Used to indicate calls or messages from contacts can bypass dnd. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_NONE](../android/service/notification/ZenPolicy.md) Used to indicate no calls or messages can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_STARRED](../android/service/notification/ZenPolicy.md) Used to indicate calls or messages from starred contacts can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_UNSET](../android/service/notification/ZenPolicy.md) Used to indicate no preference for the type of people that can bypass dnd for either calls or messages. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ALLOW](../android/service/notification/ZenPolicy.md) Indicates a type of sound or visual effect is allowed to play/show when DND is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Indicates a type of sound or visual effect is not allowed to play/show when DND is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md) Indicates no preference for whether a type of sound or visual effect is or isn't allowed to play/show when DND is active. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/notification/ZenPolicy.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/service/notification/ZenPolicy.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCallSenders](../android/service/notification/ZenPolicy.md))`()` Callers that can bypass DND. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryAlarms](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_ALARM](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryCalls](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_CALL](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryConversations](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow conversation notifications (see [NotificationChannel.getConversationId()](../android/app/NotificationChannel.md))) to play sounds and visually appear or to intercept them when DND is active. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryEvents](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_EVENT](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryMedia](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow media notifications to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryMessages](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_MESSAGE](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryReminders](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_REMINDER](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryRepeatCallers](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow repeat callers (notifications with category [Notification.CATEGORY_CALL](../android/app/Notification.md) that have recently called) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategorySystem](../android/service/notification/ZenPolicy.md))`()` Whether this policy wants to allow system sounds when DND is active. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityChannelsAllowed](../android/service/notification/ZenPolicy.md))`()` Whether this policy allows [channels](../android/app/NotificationChannel.md) marked as [NotificationChannel.canBypassDnd()](../android/app/NotificationChannel.md))to bypass DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityConversationSenders](../android/service/notification/ZenPolicy.md))`()` Conversation type that can bypass DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityMessageSenders](../android/service/notification/ZenPolicy.md))`()` Message senders that can bypass DND. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectAmbient](../android/service/notification/ZenPolicy.md))`()` Whether this policy allows notifications intercepted by DND from appearing on ambient displays on devices that support ambient display. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectBadge](../android/service/notification/ZenPolicy.md))`()` Whether this policy allows [badges](../android/app/NotificationChannel.md))from notifications intercepted by DND on devices that support badging. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectFullScreenIntent](../android/service/notification/ZenPolicy.md))`()` Whether this policy allows [full screen intents](../android/app/Notification.md) from notifications intercepted by DND. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectLights](../android/service/notification/ZenPolicy.md))`()` Whether this policy allows [lights](../android/app/NotificationChannel.md))from notifications intercepted by DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectNotificationList](../android/service/notification/ZenPolicy.md))`()` Whether this policy allows notifications intercepted by DND from appearing in notification list views like the notification shade or lockscreen on devices that support those views. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectPeek](../android/service/notification/ZenPolicy.md))`()` Whether this policy allows peeking from notifications intercepted by DND. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectStatusBar](../android/service/notification/ZenPolicy.md))`()` Whether this policy allows notifications intercepted by DND from appearing in the status bar on devices that support status bars. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/service/notification/ZenPolicy.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/service/notification/ZenPolicy.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/notification/ZenPolicy.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ZenPolicy](../android/service/notification/ZenPolicy.md)!\> | [CREATOR](../android/service/notification/ZenPolicy.md) <br /> |

## Constants

### CONVERSATION_SENDERS_ANYONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONVERSATION_SENDERS_ANYONE: Int
```

Used to indicate all conversations can bypass dnd. 

 Value: 1

### CONVERSATION_SENDERS_IMPORTANT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONVERSATION_SENDERS_IMPORTANT: Int
```

Used to indicate important conversations can bypass dnd. 

 Value: 2

### CONVERSATION_SENDERS_NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONVERSATION_SENDERS_NONE: Int
```

Used to indicate no conversations can bypass dnd. 

 Value: 3

### CONVERSATION_SENDERS_UNSET

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONVERSATION_SENDERS_UNSET: Int
```

Used to indicate no preference for the type of conversations that can bypass dnd. 

 Value: 0

### PEOPLE_TYPE_ANYONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PEOPLE_TYPE_ANYONE: Int
```

Used to indicate all calls or messages can bypass dnd. 

 Value: 1

### PEOPLE_TYPE_CONTACTS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PEOPLE_TYPE_CONTACTS: Int
```

Used to indicate calls or messages from contacts can bypass dnd. 

 Value: 2

### PEOPLE_TYPE_NONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PEOPLE_TYPE_NONE: Int
```

Used to indicate no calls or messages can bypass dnd. 

 Value: 4

### PEOPLE_TYPE_STARRED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PEOPLE_TYPE_STARRED: Int
```

Used to indicate calls or messages from starred contacts can bypass dnd. 

 Value: 3

### PEOPLE_TYPE_UNSET

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PEOPLE_TYPE_UNSET: Int
```

Used to indicate no preference for the type of people that can bypass dnd for either calls or messages. 

 Value: 0

### STATE_ALLOW

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ALLOW: Int
```

Indicates a type of sound or visual effect is allowed to play/show when DND is active. 

 Value: 1

### STATE_DISALLOW

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DISALLOW: Int
```

Indicates a type of sound or visual effect is not allowed to play/show when DND is active. 

 Value: 2

### STATE_UNSET

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_UNSET: Int
```

Indicates no preference for whether a type of sound or visual effect is or isn't allowed to play/show when DND is active. Will default to the current set policy. 

 Value: 0

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getPriorityCallSenders

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCallSenders(): Int
```

Callers that can bypass DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_UNSET](../android/service/notification/ZenPolicy.md), [PEOPLE_TYPE_ANYONE](../android/service/notification/ZenPolicy.md), [PEOPLE_TYPE_CONTACTS](../android/service/notification/ZenPolicy.md), [PEOPLE_TYPE_STARRED](../android/service/notification/ZenPolicy.md) or [PEOPLE_TYPE_NONE](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#PEOPLE_TYPE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#PEOPLE_TYPE_ANYONE](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#PEOPLE_TYPE_CONTACTS](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#PEOPLE_TYPE_STARRED](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#PEOPLE_TYPE_NONE](../android/service/notification/ZenPolicy.md) |

### getPriorityCategoryAlarms

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryAlarms(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_ALARM](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active. When alarms are [disallowed](../android/service/notification/ZenPolicy.md), the alarm stream will be muted when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityCategoryCalls

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryCalls(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_CALL](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active. Types of callers that are allowed are specified by [getPriorityCallSenders()](../android/service/notification/ZenPolicy.md)).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityCategoryConversations

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryConversations(): Int
```

Whether this policy wants to allow conversation notifications (see [NotificationChannel.getConversationId()](../android/app/NotificationChannel.md))) to play sounds and visually appear or to intercept them when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityCategoryEvents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryEvents(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_EVENT](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityCategoryMedia

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryMedia(): Int
```

Whether this policy wants to allow media notifications to play sounds and visually appear or to intercept them when DND is active. When media is [disallowed](../android/service/notification/ZenPolicy.md), the media stream will be muted when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityCategoryMessages

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryMessages(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_MESSAGE](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active. Types of message senders that are allowed are specified by [getPriorityMessageSenders](../android/service/notification/ZenPolicy.md)).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityCategoryReminders

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryReminders(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_REMINDER](../android/app/Notification.md) to play sounds and visually appear or to intercept them when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityCategoryRepeatCallers

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryRepeatCallers(): Int
```

Whether this policy wants to allow repeat callers (notifications with category [Notification.CATEGORY_CALL](../android/app/Notification.md) that have recently called) to play sounds and visually appear or to intercept them when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityCategorySystem

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategorySystem(): Int
```

Whether this policy wants to allow system sounds when DND is active. When system is [STATE_DISALLOW](../android/service/notification/ZenPolicy.md), the system stream will be muted when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](../android/service/notification/ZenPolicy.md), [STATE_ALLOW](../android/service/notification/ZenPolicy.md) or [STATE_DISALLOW](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityChannelsAllowed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityChannelsAllowed(): Int
```

Whether this policy allows [channels](../android/app/NotificationChannel.md) marked as [NotificationChannel.canBypassDnd()](../android/app/NotificationChannel.md))to bypass DND. If [STATE_ALLOW](../android/service/notification/ZenPolicy.md), these channels may bypass; if [STATE_DISALLOW](../android/service/notification/ZenPolicy.md), then even notifications from channels with [NotificationChannel.canBypassDnd()](../android/app/NotificationChannel.md))will be intercepted.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getPriorityConversationSenders

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityConversationSenders(): Int
```

Conversation type that can bypass DND.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_UNSET](../android/service/notification/ZenPolicy.md), [CONVERSATION_SENDERS_ANYONE](../android/service/notification/ZenPolicy.md), [CONVERSATION_SENDERS_IMPORTANT](../android/service/notification/ZenPolicy.md), [CONVERSATION_SENDERS_NONE](../android/service/notification/ZenPolicy.md). Value is [android.service.notification.ZenPolicy#CONVERSATION_SENDERS_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#CONVERSATION_SENDERS_ANYONE](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#CONVERSATION_SENDERS_IMPORTANT](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#CONVERSATION_SENDERS_NONE](../android/service/notification/ZenPolicy.md) |

### getPriorityMessageSenders

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityMessageSenders(): Int
```

Message senders that can bypass DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_UNSET](../android/service/notification/ZenPolicy.md), [PEOPLE_TYPE_ANYONE](../android/service/notification/ZenPolicy.md), [PEOPLE_TYPE_CONTACTS](../android/service/notification/ZenPolicy.md), [PEOPLE_TYPE_STARRED](../android/service/notification/ZenPolicy.md) or [PEOPLE_TYPE_NONE](../android/service/notification/ZenPolicy.md) Value is [android.service.notification.ZenPolicy#PEOPLE_TYPE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#PEOPLE_TYPE_ANYONE](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#PEOPLE_TYPE_CONTACTS](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#PEOPLE_TYPE_STARRED](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#PEOPLE_TYPE_NONE](../android/service/notification/ZenPolicy.md) |

### getVisualEffectAmbient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectAmbient(): Int
```

Whether this policy allows notifications intercepted by DND from appearing on ambient displays on devices that support ambient display.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getVisualEffectBadge

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectBadge(): Int
```

Whether this policy allows [badges](../android/app/NotificationChannel.md))from notifications intercepted by DND on devices that support badging.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getVisualEffectFullScreenIntent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectFullScreenIntent(): Int
```

Whether this policy allows [full screen intents](../android/app/Notification.md) from notifications intercepted by DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getVisualEffectLights

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectLights(): Int
```

Whether this policy allows [lights](../android/app/NotificationChannel.md))from notifications intercepted by DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getVisualEffectNotificationList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectNotificationList(): Int
```

Whether this policy allows notifications intercepted by DND from appearing in notification list views like the notification shade or lockscreen on devices that support those views.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getVisualEffectPeek

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectPeek(): Int
```

Whether this policy allows peeking from notifications intercepted by DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### getVisualEffectStatusBar

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectStatusBar(): Int
```

Whether this policy allows notifications intercepted by DND from appearing in the status bar on devices that support status bars.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](../android/service/notification/ZenPolicy.md), [android.service.notification.ZenPolicy#STATE_ALLOW](../android/service/notification/ZenPolicy.md), or [android.service.notification.ZenPolicy#STATE_DISALLOW](../android/service/notification/ZenPolicy.md) |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ZenPolicy!>
```
