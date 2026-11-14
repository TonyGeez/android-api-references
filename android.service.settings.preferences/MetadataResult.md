Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MetadataResult

```
class MetadataResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.settings.preferences.MetadataResult](MetadataResult.md) |

Result object given a corresponding `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataRequest`.

- If the request was successful, `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#getResultCode()` will be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#RESULT_OK:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#getMetadataList()` will be populated with metadata for all available preferences within this application.
- If the request is unsuccessful, `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#getResultCode()` be a value other than `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#RESULT_OK:kotlin.Int` - see documentation for those possibilities to understand the cause of the failure.

<br />

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult.Builder` Builder to construct `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#RESULT_INTERNAL_ERROR:kotlin.Int` API call failed due to an issue with the service binding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#RESULT_OK:kotlin.Int` Request is successful. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#RESULT_UNSUPPORTED:kotlin.Int` No preferences in this application support this API. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SettingsPreferenceMetadata](SettingsPreferenceMetadata.md)!\> | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#getMetadataList()()` Returns the list of available Preference Metadata. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#getResultCode()()` Returns the result code indicating status of the request. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [MetadataResult](MetadataResult.md)!\> | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#CREATOR:android.os.Parcelable.Creator` Parcelable Creator for `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#`. |

## Constants

### RESULT_INTERNAL_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INTERNAL_ERROR: Int
```

API call failed due to an issue with the service binding.

Retry may succeed.

 Value: 2

### RESULT_OK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_OK: Int
```

Request is successful.

 Value: 0

### RESULT_UNSUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_UNSUPPORTED: Int
```

No preferences in this application support this API.

Retry not advised.

 Value: 1

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getMetadataList

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMetadataList(): MutableList<SettingsPreferenceMetadata!>
```

Returns the list of available Preference Metadata.

This instance is shared so this list should not be modified.

### getResultCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultCode(): Int
```

Returns the result code indicating status of the request.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#RESULT_OK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#RESULT_UNSUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#RESULT_INTERNAL_ERROR:kotlin.Int` |

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
static val CREATOR: Parcelable.Creator<MetadataResult!>
```

Parcelable Creator for `https://developer.android.com/reference/kotlin/android/service/settings/preferences/MetadataResult#`.
