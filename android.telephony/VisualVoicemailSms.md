Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VisualVoicemailSms

Kotlin | [Java](https://developer.android.com/reference/android/telephony/VisualVoicemailSms "View this page in Java")
| --- | --- |

```
class VisualVoicemailSms : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.VisualVoicemailSms](https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#) |

Represents the content of a visual voicemail SMS. If a incoming SMS matches the `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings` set by the default dialer, `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailService#onSmsReceived(android.telephony.VisualVoicemailService.VisualVoicemailTask,%20android.telephony.VisualVoicemailSms)` will be called.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#getFields()()` The key-value pairs sent by the SMS, or `null` if the framework cannot parse the SMS as voicemail but the carrier pattern indicates it is. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#getMessageBody()()` Raw message body of the received SMS. |
| --- | --- |
| [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#)! | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#getPhoneAccountHandle()()` The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` that received the SMS. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#getPrefix()()` The event type of the SMS or `null` if the framework cannot parse the SMS as voicemail but the carrier pattern indicates it is. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [VisualVoicemailSms](https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#)!\> | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSms#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getFields

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFields(): Bundle!
```

The key-value pairs sent by the SMS, or `null` if the framework cannot parse the SMS as voicemail but the carrier pattern indicates it is. The interpretation of the fields is carrier dependent.

### getMessageBody

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMessageBody(): String!
```

Raw message body of the received SMS.

### getPhoneAccountHandle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPhoneAccountHandle(): PhoneAccountHandle!
```

The `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle.html#` that received the SMS.

### getPrefix

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPrefix(): String!
```

The event type of the SMS or `null` if the framework cannot parse the SMS as voicemail but the carrier pattern indicates it is. Common values are "SYNC" or "STATUS".

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<VisualVoicemailSms!>
```
