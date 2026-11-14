Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetValueRequest

```
class GetValueRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.settings.preferences.GetValueRequest](https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#) |

Request parameters to retrieve the current value of a Settings Preference.

This object passed to `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SettingsPreferenceService#onGetPreferenceValue(android.service.settings.preferences.GetValueRequest,%20android.os.OutcomeReceiver)` will result in a `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult`.

- `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#getScreenKey()` is a parameter to distinguish the container screen of a preference as a preference key may not be unique within its application.
- `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#getPreferenceKey()` is a parameter to identify the preference for which the value is being requested. These keys will be unique with their Preference Screen, but may not be unique within their application, so it is required to pair this with `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#getScreenKey()` to ensure this request matches the intended target.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest.Builder` Builder to construct `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#`. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#getPreferenceKey()()` Returns the key of requested Preference. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#getScreenKey()()` Returns the screen key of requested Preference. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GetValueRequest](https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#)!\> | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#CREATOR:android.os.Parcelable.Creator` Parcelable Creator for `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#`. |

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

### getPreferenceKey

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPreferenceKey(): String
```

Returns the key of requested Preference.

### getScreenKey

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScreenKey(): String
```

Returns the screen key of requested Preference.

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<GetValueRequest!>
```

Parcelable Creator for `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueRequest#`.
