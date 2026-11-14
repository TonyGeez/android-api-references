Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConversationAction

Kotlin | [Java](https://developer.android.com/reference/android/view/textclassifier/ConversationAction "View this page in Java")
| --- | --- |

```
class ConversationAction : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.ConversationAction](https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#) |

Represents the action suggested by a `https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier` on a given conversation.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction.Builder` Builder class to construct `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#`. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_CALL_PHONE:kotlin.String` Indicates an action to call a phone number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_CREATE_REMINDER:kotlin.String` Indicates an action to create a reminder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_OPEN_URL:kotlin.String` Indicates an action to open an URL. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_SEND_EMAIL:kotlin.String` Indicates an action to send an email. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_SEND_SMS:kotlin.String` Indicates an action to send a SMS. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_SHARE_LOCATION:kotlin.String` Indicates an action to reply with a location. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_TEXT_REPLY:kotlin.String` Indicates an action to reply with a text message. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_TRACK_FLIGHT:kotlin.String` Indicates an action to track a flight. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_VIEW_CALENDAR:kotlin.String` Indicates an action to view a calendar at a specified time. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_VIEW_MAP:kotlin.String` Indicates an action to view the map at a specified location. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [RemoteAction](https://developer.android.com/reference/kotlin/android/app/RemoteAction.html#)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#getAction()()` Returns a RemoteAction object, which contains the icon, label and a PendingIntent, for the specified action type. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#getConfidenceScore()()` Returns the confidence score for the specified action. |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#getExtras()()` Returns the extended data related to this conversation action. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#getTextReply()()` Returns the text reply that could be sent as a reply to the given conversation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#getType()()` Returns the type of this action, for example, `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_VIEW_CALENDAR:kotlin.String`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ConversationAction](https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#)!\> | `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### TYPE_CALL_PHONE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CALL_PHONE: String
```

Indicates an action to call a phone number.

 Value: "call_phone"

### TYPE_CREATE_REMINDER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_CREATE_REMINDER: String
```

Indicates an action to create a reminder.

 Value: "create_reminder"

### TYPE_OPEN_URL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_OPEN_URL: String
```

Indicates an action to open an URL.

 Value: "open_url"

### TYPE_SEND_EMAIL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SEND_EMAIL: String
```

Indicates an action to send an email.

 Value: "send_email"

### TYPE_SEND_SMS

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SEND_SMS: String
```

Indicates an action to send a SMS.

 Value: "send_sms"

### TYPE_SHARE_LOCATION

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SHARE_LOCATION: String
```

Indicates an action to reply with a location.

 Value: "share_location"

### TYPE_TEXT_REPLY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_TEXT_REPLY: String
```

Indicates an action to reply with a text message.

 Value: "text_reply"

### TYPE_TRACK_FLIGHT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_TRACK_FLIGHT: String
```

Indicates an action to track a flight.

 Value: "track_flight"

### TYPE_VIEW_CALENDAR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VIEW_CALENDAR: String
```

Indicates an action to view a calendar at a specified time.

 Value: "view_calendar"

### TYPE_VIEW_MAP

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_VIEW_MAP: String
```

Indicates an action to view the map at a specified location.

 Value: "view_map"

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAction

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAction(): RemoteAction?
```

Returns a RemoteAction object, which contains the icon, label and a PendingIntent, for the specified action type.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/RemoteAction.html#?` | This value may be `null`. |

### getConfidenceScore

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConfidenceScore(): Float
```

Returns the confidence score for the specified action. The value ranges from 0 (low confidence) to 1 (high confidence).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 1.0f inclusive |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle
```

Returns the extended data related to this conversation action.

**NOTE:**Do not modify this bundle.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

### getTextReply

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextReply(): CharSequence?
```

Returns the text reply that could be sent as a reply to the given conversation.

This is only available when the type of the action is `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_TEXT_REPLY:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | This value may be `null`. |

### getType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): String
```

Returns the type of this action, for example, `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_VIEW_CALENDAR:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_VIEW_CALENDAR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_VIEW_MAP:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_TRACK_FLIGHT:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_OPEN_URL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_SEND_SMS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_CALL_PHONE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_SEND_EMAIL:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_TEXT_REPLY:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_CREATE_REMINDER:kotlin.String` - `https://developer.android.com/reference/kotlin/android/view/textclassifier/ConversationAction#TYPE_SHARE_LOCATION:kotlin.String` |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ConversationAction!>
```
