Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetValueResult

```
class GetValueResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.settings.preferences.GetValueResult](GetValueResult.md) |

Result object given a corresponding GetValueRequest.

- If the request was successful, getResultCode will be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_OK:kotlin.Int`, getValue will be populated with the settings preference value and getMetadata will be populated with its metadata.
- If the request is unsuccessful, getResultCode be a value other than `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_OK:kotlin.Int` - see documentation for those possibilities to understand the cause of the failure.

<br />

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult.Builder` Builder to construct GetValueResult. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_DISALLOW:kotlin.Int` Requested preference is not allowed for access in this API under the current device policy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_INTERNAL_ERROR:kotlin.Int` API call failed due to an issue with the service binding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_INVALID_REQUEST:kotlin.Int` Request object is not valid. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_OK:kotlin.Int` Request is successful. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_REQUIRE_APP_PERMISSION:kotlin.Int` Requested preference requires permissions not held by the calling application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_UNAVAILABLE:kotlin.Int` Preference is currently not available, likely due to device state or the state of a dependency. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_UNSUPPORTED:kotlin.Int` Requested preference is not supported by this API. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [SettingsPreferenceMetadata](SettingsPreferenceMetadata.md)? | getMetadata Returns the metadata of requested Preference if request successful. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getResultCode Returns the result code indicating status of the request. |
| --- | --- |
| [SettingsPreferenceValue](SettingsPreferenceValue.md)? | getValue Returns the value of requested Preference if request successful. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GetValueResult](GetValueResult.md)!\> | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#CREATOR:android.os.Parcelable.Creator` Parcelable Creator for GetValueResult. |

## Constants

### RESULT_DISALLOW

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_DISALLOW: Int
```

Requested preference is not allowed for access in this API under the current device policy.

Retry may succeed if underlying conditions change.

 Value: 4

### RESULT_INTERNAL_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INTERNAL_ERROR: Int
```

API call failed due to an issue with the service binding.

Retry may succeed.

 Value: 6

### RESULT_INVALID_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INVALID_REQUEST: Int
```

Request object is not valid.

Retry not advised with current parameters.

 Value: 5

### RESULT_OK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_OK: Int
```

Request is successful.

 Value: 0

### RESULT_REQUIRE_APP_PERMISSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_REQUIRE_APP_PERMISSION: Int
```

Requested preference requires permissions not held by the calling application.

Retry may succeed if necessary permissions are obtained.

 Value: 3

### RESULT_UNAVAILABLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_UNAVAILABLE: Int
```

Preference is currently not available, likely due to device state or the state of a dependency.

Retry may succeed if underlying conditions change.

 Value: 2

### RESULT_UNSUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_UNSUPPORTED: Int
```

Requested preference is not supported by this API.

Retry not advised.

 Value: 1

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

### getMetadata

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMetadata(): SettingsPreferenceMetadata?
```

Returns the metadata of requested Preference if request successful.

### getResultCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultCode(): Int
```

Returns the result code indicating status of the request.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_OK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_UNSUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_REQUIRE_APP_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_DISALLOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_INVALID_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/GetValueResult#RESULT_INTERNAL_ERROR:kotlin.Int` |

### getValue

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getValue(): SettingsPreferenceValue?
```

Returns the value of requested Preference if request successful.

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
static val CREATOR: Parcelable.Creator<GetValueResult!>
```

Parcelable Creator for GetValueResult.
