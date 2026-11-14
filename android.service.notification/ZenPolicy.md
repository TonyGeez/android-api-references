# ZenPolicy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZenPolicy

Kotlin| [Java](https://developer.android.com/reference/android/service/notification/ZenPolicy "View this page in Java") 

```
class ZenPolicy : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.notification.ZenPolicy](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#) |

ZenPolicy determines whether to allow certain notifications and their corresponding sounds to play when a device is in Do Not Disturb mode. ZenPolicy also dictates the visual effects of notifications that are intercepted when a device is in Do Not Disturb mode.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy.Builder) Builder class for [ZenPolicy](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#) objects. |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_ANYONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_ANYONE:kotlin.Int) Used to indicate all conversations can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_IMPORTANT](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_IMPORTANT:kotlin.Int) Used to indicate important conversations can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_NONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_NONE:kotlin.Int) Used to indicate no conversations can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_UNSET:kotlin.Int) Used to indicate no preference for the type of conversations that can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_ANYONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_ANYONE:kotlin.Int) Used to indicate all calls or messages can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_CONTACTS](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_CONTACTS:kotlin.Int) Used to indicate calls or messages from contacts can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_NONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_NONE:kotlin.Int) Used to indicate no calls or messages can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_STARRED](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_STARRED:kotlin.Int) Used to indicate calls or messages from starred contacts can bypass dnd. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_UNSET:kotlin.Int) Used to indicate no preference for the type of people that can bypass dnd for either calls or messages. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) Indicates a type of sound or visual effect is allowed to play/show when DND is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Indicates a type of sound or visual effect is not allowed to play/show when DND is active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int) Indicates no preference for whether a type of sound or visual effect is or isn't allowed to play/show when DND is active. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCallSenders](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCallSenders())`()` Callers that can bypass DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryAlarms](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategoryAlarms())`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_ALARM](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_ALARM:kotlin.String) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryCalls](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategoryCalls())`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_CALL](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_CALL:kotlin.String) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryConversations](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategoryConversations())`()` Whether this policy wants to allow conversation notifications (see [NotificationChannel.getConversationId()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#getConversationId())) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryEvents](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategoryEvents())`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_EVENT](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_EVENT:kotlin.String) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryMedia](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategoryMedia())`()` Whether this policy wants to allow media notifications to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryMessages](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategoryMessages())`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_MESSAGE](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_MESSAGE:kotlin.String) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryReminders](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategoryReminders())`()` Whether this policy wants to allow notifications with category [Notification.CATEGORY_REMINDER](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_REMINDER:kotlin.String) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategoryRepeatCallers](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategoryRepeatCallers())`()` Whether this policy wants to allow repeat callers (notifications with category [Notification.CATEGORY_CALL](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_CALL:kotlin.String) that have recently called) to play sounds and visually appear or to intercept them when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityCategorySystem](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCategorySystem())`()` Whether this policy wants to allow system sounds when DND is active. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityChannelsAllowed](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityChannelsAllowed())`()` Whether this policy allows [channels](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#) marked as [NotificationChannel.canBypassDnd()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#canBypassDnd())to bypass DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityConversationSenders](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityConversationSenders())`()` Conversation type that can bypass DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPriorityMessageSenders](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityMessageSenders())`()` Message senders that can bypass DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectAmbient](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getVisualEffectAmbient())`()` Whether this policy allows notifications intercepted by DND from appearing on ambient displays on devices that support ambient display. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectBadge](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getVisualEffectBadge())`()` Whether this policy allows [badges](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#canShowBadge())from notifications intercepted by DND on devices that support badging. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectFullScreenIntent](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getVisualEffectFullScreenIntent())`()` Whether this policy allows [full screen intents](https://developer.android.com/reference/kotlin/android/app/Notification.html#fullScreenIntent:android.app.PendingIntent) from notifications intercepted by DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectLights](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getVisualEffectLights())`()` Whether this policy allows [lights](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#shouldShowLights())from notifications intercepted by DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectNotificationList](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getVisualEffectNotificationList())`()` Whether this policy allows notifications intercepted by DND from appearing in notification list views like the notification shade or lockscreen on devices that support those views. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectPeek](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getVisualEffectPeek())`()` Whether this policy allows peeking from notifications intercepted by DND. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVisualEffectStatusBar](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getVisualEffectStatusBar())`()` Whether this policy allows notifications intercepted by DND from appearing in the status bar on devices that support status bars. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ZenPolicy](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_UNSET:kotlin.Int), [PEOPLE_TYPE_ANYONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_ANYONE:kotlin.Int), [PEOPLE_TYPE_CONTACTS](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_CONTACTS:kotlin.Int), [PEOPLE_TYPE_STARRED](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_STARRED:kotlin.Int) or [PEOPLE_TYPE_NONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_NONE:kotlin.Int) Value is [android.service.notification.ZenPolicy#PEOPLE_TYPE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#PEOPLE_TYPE_ANYONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_ANYONE:kotlin.Int), [android.service.notification.ZenPolicy#PEOPLE_TYPE_CONTACTS](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_CONTACTS:kotlin.Int), [android.service.notification.ZenPolicy#PEOPLE_TYPE_STARRED](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_STARRED:kotlin.Int), or [android.service.notification.ZenPolicy#PEOPLE_TYPE_NONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_NONE:kotlin.Int) |

### getPriorityCategoryAlarms

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryAlarms(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_ALARM](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_ALARM:kotlin.String) to play sounds and visually appear or to intercept them when DND is active. When alarms are [disallowed](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int), the alarm stream will be muted when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityCategoryCalls

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryCalls(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_CALL](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_CALL:kotlin.String) to play sounds and visually appear or to intercept them when DND is active. Types of callers that are allowed are specified by [getPriorityCallSenders()](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityCallSenders()).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityCategoryConversations

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryConversations(): Int
```

Whether this policy wants to allow conversation notifications (see [NotificationChannel.getConversationId()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#getConversationId())) to play sounds and visually appear or to intercept them when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityCategoryEvents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryEvents(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_EVENT](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_EVENT:kotlin.String) to play sounds and visually appear or to intercept them when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityCategoryMedia

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryMedia(): Int
```

Whether this policy wants to allow media notifications to play sounds and visually appear or to intercept them when DND is active. When media is [disallowed](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int), the media stream will be muted when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityCategoryMessages

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryMessages(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_MESSAGE](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_MESSAGE:kotlin.String) to play sounds and visually appear or to intercept them when DND is active. Types of message senders that are allowed are specified by [getPriorityMessageSenders](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#getPriorityMessageSenders()).

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityCategoryReminders

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryReminders(): Int
```

Whether this policy wants to allow notifications with category [Notification.CATEGORY_REMINDER](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_REMINDER:kotlin.String) to play sounds and visually appear or to intercept them when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityCategoryRepeatCallers

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategoryRepeatCallers(): Int
```

Whether this policy wants to allow repeat callers (notifications with category [Notification.CATEGORY_CALL](https://developer.android.com/reference/kotlin/android/app/Notification.html#CATEGORY_CALL:kotlin.String) that have recently called) to play sounds and visually appear or to intercept them when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityCategorySystem

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityCategorySystem(): Int
```

Whether this policy wants to allow system sounds when DND is active. When system is [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int), the system stream will be muted when DND is active.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int) or [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityChannelsAllowed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityChannelsAllowed(): Int
```

Whether this policy allows [channels](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#) marked as [NotificationChannel.canBypassDnd()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#canBypassDnd())to bypass DND. If [STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), these channels may bypass; if [STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int), then even notifications from channels with [NotificationChannel.canBypassDnd()](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#canBypassDnd())will be intercepted.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getPriorityConversationSenders

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityConversationSenders(): Int
```

Conversation type that can bypass DND.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONVERSATION_SENDERS_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_UNSET:kotlin.Int), [CONVERSATION_SENDERS_ANYONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_ANYONE:kotlin.Int), [CONVERSATION_SENDERS_IMPORTANT](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_IMPORTANT:kotlin.Int), [CONVERSATION_SENDERS_NONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_NONE:kotlin.Int). Value is [android.service.notification.ZenPolicy#CONVERSATION_SENDERS_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#CONVERSATION_SENDERS_ANYONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_ANYONE:kotlin.Int), [android.service.notification.ZenPolicy#CONVERSATION_SENDERS_IMPORTANT](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_IMPORTANT:kotlin.Int), or [android.service.notification.ZenPolicy#CONVERSATION_SENDERS_NONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#CONVERSATION_SENDERS_NONE:kotlin.Int) |

### getPriorityMessageSenders

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPriorityMessageSenders(): Int
```

Message senders that can bypass DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PEOPLE_TYPE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_UNSET:kotlin.Int), [PEOPLE_TYPE_ANYONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_ANYONE:kotlin.Int), [PEOPLE_TYPE_CONTACTS](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_CONTACTS:kotlin.Int), [PEOPLE_TYPE_STARRED](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_STARRED:kotlin.Int) or [PEOPLE_TYPE_NONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_NONE:kotlin.Int) Value is [android.service.notification.ZenPolicy#PEOPLE_TYPE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#PEOPLE_TYPE_ANYONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_ANYONE:kotlin.Int), [android.service.notification.ZenPolicy#PEOPLE_TYPE_CONTACTS](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_CONTACTS:kotlin.Int), [android.service.notification.ZenPolicy#PEOPLE_TYPE_STARRED](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_STARRED:kotlin.Int), or [android.service.notification.ZenPolicy#PEOPLE_TYPE_NONE](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#PEOPLE_TYPE_NONE:kotlin.Int) |

### getVisualEffectAmbient

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectAmbient(): Int
```

Whether this policy allows notifications intercepted by DND from appearing on ambient displays on devices that support ambient display.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getVisualEffectBadge

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectBadge(): Int
```

Whether this policy allows [badges](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#canShowBadge())from notifications intercepted by DND on devices that support badging.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getVisualEffectFullScreenIntent

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectFullScreenIntent(): Int
```

Whether this policy allows [full screen intents](https://developer.android.com/reference/kotlin/android/app/Notification.html#fullScreenIntent:android.app.PendingIntent) from notifications intercepted by DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getVisualEffectLights

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectLights(): Int
```

Whether this policy allows [lights](https://developer.android.com/reference/kotlin/android/app/NotificationChannel.html#shouldShowLights())from notifications intercepted by DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getVisualEffectNotificationList

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectNotificationList(): Int
```

Whether this policy allows notifications intercepted by DND from appearing in notification list views like the notification shade or lockscreen on devices that support those views.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getVisualEffectPeek

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectPeek(): Int
```

Whether this policy allows peeking from notifications intercepted by DND.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

### getVisualEffectStatusBar

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVisualEffectStatusBar(): Int
```

Whether this policy allows notifications intercepted by DND from appearing in the status bar on devices that support status bars.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.service.notification.ZenPolicy#STATE_UNSET](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_UNSET:kotlin.Int), [android.service.notification.ZenPolicy#STATE_ALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_ALLOW:kotlin.Int), or [android.service.notification.ZenPolicy#STATE_DISALLOW](https://developer.android.com/reference/kotlin/android/service/notification/ZenPolicy#STATE_DISALLOW:kotlin.Int) |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ZenPolicy!>
```
