Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VisualVoicemailSmsFilterSettings

Kotlin | [Java](VisualVoicemailSmsFilterSettings.md)
| --- | --- |

```
class VisualVoicemailSmsFilterSettings : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.VisualVoicemailSmsFilterSettings](VisualVoicemailSmsFilterSettings.md) |

Class to represent various settings for the visual voicemail SMS filter. When the filter is enabled, incoming SMS matching the generalized OMTP format:

\[clientPrefix\]:\[prefix\]:(\[key\]=\[value\];)\*

will be regarded as a visual voicemail SMS, and removed before reaching the SMS provider. The VisualVoicemailService in the current default dialer will be bound and onSmsReceived will called with the information extracted from the SMS.

Use `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings.Builder` to construct this class.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings.Builder` Builder class for VisualVoicemailSmsFilterSettings objects. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#DESTINATION_PORT_ANY:kotlin.Int` The visual voicemail SMS message does not have to be a data SMS, and can be directed to any port. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#DESTINATION_PORT_DATA_SMS:kotlin.Int` The visual voicemail SMS message can be directed to any port, but must be a data SMS. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [VisualVoicemailSmsFilterSettings](VisualVoicemailSmsFilterSettings.md)!\> | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#CREATOR:android.os.Parcelable.Creator` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#clientPrefix:kotlin.String` The client prefix for the visual voicemail SMS filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#destinationPort:kotlin.Int` The destination port for the visual voicemail SMS filter, or `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#DESTINATION_PORT_ANY:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#DESTINATION_PORT_DATA_SMS:kotlin.Int` |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#originatingNumbers:kotlin.collections.MutableList` The originating number allow list for the visual voicemail SMS filter of a phone account. |

## Constants

### DESTINATION_PORT_ANY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DESTINATION_PORT_ANY: Int
```

The visual voicemail SMS message does not have to be a data SMS, and can be directed to any port.

 Value: -1

### DESTINATION_PORT_DATA_SMS

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DESTINATION_PORT_DATA_SMS: Int
```

The visual voicemail SMS message can be directed to any port, but must be a data SMS.

 Value: -2

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

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
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<VisualVoicemailSmsFilterSettings!>
```

### clientPrefix

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val clientPrefix: String!
```

The client prefix for the visual voicemail SMS filter. The client prefix will appear at the start of a visual voicemail SMS message, followed by a colon(:).

### destinationPort

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val destinationPort: Int
```

The destination port for the visual voicemail SMS filter, or `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#DESTINATION_PORT_ANY:kotlin.Int`, or `https://developer.android.com/reference/kotlin/android/telephony/VisualVoicemailSmsFilterSettings#DESTINATION_PORT_DATA_SMS:kotlin.Int`

### originatingNumbers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val originatingNumbers: MutableList<String!>!
```

The originating number allow list for the visual voicemail SMS filter of a phone account. If the list is not null only the SMS messages from a number in the list can be considered as a visual voicemail SMS. Otherwise, messages from any address will be considered.
