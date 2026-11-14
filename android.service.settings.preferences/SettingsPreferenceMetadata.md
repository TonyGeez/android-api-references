Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SettingsPreferenceMetadata

```
class SettingsPreferenceMetadata : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.settings.preferences.SettingsPreferenceMetadata](SettingsPreferenceMetadata.md) |

Data object representation of a Settings Preference definition and state.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata.Builder` Builder to construct SettingsPreferenceMetadata. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#DEEPLINK_ONLY:kotlin.Int` Indicates preference is write-sensitive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#EXPECT_POST_CONFIRMATION:kotlin.Int` Indicates preference is mildly write-sensitive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#NO_DIRECT_ACCESS:kotlin.Int` Indicates preference is highly write-sensitivity and carries significant user-risk. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#NO_SENSITIVITY:kotlin.Int` Indicates preference is not write-sensitive. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Bundle](../android.os/Bundle.md) | getExtras Returns any additional fields specific to this preference. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getKey Returns the key of Preference. |
| --- | --- |
| [Intent](../android.content/Intent.md)? | getLaunchIntent Returns the intent to launch the host app page for this Preference. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getReadPermissions Returns the permissions required to read this Preference's value. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getScreenKey Returns the screen key of Preference. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getSummary Returns the summary of Preference. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getTitle Returns the title of Preference. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getWritePermissions Returns the permissions required to write this Preference's value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getWriteSensitivity Returns the write-level sensitivity of Preference. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAvailable Returns whether Preference is available. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEnabled Returns whether Preference is enabled. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isRestricted Returns whether Preference is restricted. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isWritable Returns whether Preference is writable. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SettingsPreferenceMetadata](SettingsPreferenceMetadata.md)!\> | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#CREATOR:android.os.Parcelable.Creator` Parcelable Creator for SettingsPreferenceMetadata. |

## Constants

### DEEPLINK_ONLY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEEPLINK_ONLY: Int
```

Indicates preference is write-sensitive.

This preference cannot be changed through this API; instead a deeplink to the Preference's page should be used instead, accessible via getLaunchIntent.

 Value: 2

### EXPECT_POST_CONFIRMATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXPECT_POST_CONFIRMATION: Int
```

Indicates preference is mildly write-sensitive.

In addition to necessary permissions, after writing its value the user should be given the option to revert back.

 Value: 1

### NO_DIRECT_ACCESS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_DIRECT_ACCESS: Int
```

Indicates preference is highly write-sensitivity and carries significant user-risk.

This Preference cannot be changed through this API and no direct deeplink is available. Other Metadata is still available.

 Value: 3

### NO_SENSITIVITY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NO_SENSITIVITY: Int
```

Indicates preference is not write-sensitive.

Its value is writable without explicit consent, assuming all necessary permissions are granted.

 Value: 0

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getExtras

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle
```

Returns any additional fields specific to this preference.

Treat all data as optional. This may contain unstructured data for a given preference, where the type and format of this data may only known by inspecting the source code of that preference. As such, any access of this data must handle failures gracefully to account for changing or missing data.

### getKey

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKey(): String
```

Returns the key of Preference.

### getLaunchIntent

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLaunchIntent(): Intent?
```

Returns the intent to launch the host app page for this Preference.

### getReadPermissions

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReadPermissions(): MutableList<String!>
```

Returns the permissions required to read this Preference's value.

May be empty.

### getScreenKey

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScreenKey(): String
```

Returns the screen key of Preference.

### getSummary

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSummary(): String?
```

Returns the summary of Preference.

### getTitle

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTitle(): String?
```

Returns the title of Preference.

### getWritePermissions

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWritePermissions(): MutableList<String!>
```

Returns the permissions required to write this Preference's value.

May be empty.

### getWriteSensitivity

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWriteSensitivity(): Int
```

Returns the write-level sensitivity of Preference.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#NO_SENSITIVITY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#EXPECT_POST_CONFIRMATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#DEEPLINK_ONLY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceMetadata#NO_DIRECT_ACCESS:kotlin.Int` |

### isAvailable

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAvailable(): Boolean
```

Returns whether Preference is available.

### isEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEnabled(): Boolean
```

Returns whether Preference is enabled.

### isRestricted

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRestricted(): Boolean
```

Returns whether Preference is restricted.

If true, this means the Preference is treated as a Restricted Preference which indicates that it could be conditionally disabled/unavailable due to admin settings.

### isWritable

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isWritable(): Boolean
```

Returns whether Preference is writable.

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SettingsPreferenceMetadata!>
```

Parcelable Creator for SettingsPreferenceMetadata.
