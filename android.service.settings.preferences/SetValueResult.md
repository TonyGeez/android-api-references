Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SetValueResult

```
class SetValueResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.settings.preferences.SetValueResult](../android/service/settings/preferences/SetValueResult.md) |

Result object given a corresponding `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueRequest`.

- If the request was successful, `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#getResultCode()` will be `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_OK:kotlin.Int`.
- If the request is unsuccessful, `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#getResultCode()` be a value other than `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_OK:kotlin.Int` - see documentation for those possibilities to understand the cause of the failure.

<br />

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult.Builder` Builder to construct `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_DISABLED:kotlin.Int` Requested preference is disabled, thus unable to be set in this state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_DISALLOW:kotlin.Int` Requested preference is not allowed for access in this API under the current device policy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_INTERNAL_ERROR:kotlin.Int` API call failed due to an issue with the service binding. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_INVALID_REQUEST:kotlin.Int` Request object is not valid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_OK:kotlin.Int` Request is successful and the value was set. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_REQUIRE_APP_PERMISSION:kotlin.Int` Requested preference requires permissions not held by the calling application. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_REQUIRE_USER_CONSENT:kotlin.Int` User consent was not approved for this operation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_RESTRICTED:kotlin.Int` Requested preference is restricted, thus unable to be set under this policy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_UNAVAILABLE:kotlin.Int` Preference is currently not available, likely due to device state or the state of a dependency. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_UNSUPPORTED:kotlin.Int` Requested preference is not supported by this API. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#getResultCode()()` Returns the result code indicating status of the request. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SetValueResult](../android/service/settings/preferences/SetValueResult.md)!\> | `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#CREATOR:android.os.Parcelable.Creator` Parcelable Creator for `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#`. |

## Constants

### RESULT_DISABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_DISABLED: Int
```

Requested preference is disabled, thus unable to be set in this state.

Retry may succeed if underlying conditions change.

 Value: 2

### RESULT_DISALLOW

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_DISALLOW: Int
```

Requested preference is not allowed for access in this API under the current device policy.

Retry may succeed if underlying conditions change.

 Value: 7

### RESULT_INTERNAL_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INTERNAL_ERROR: Int
```

API call failed due to an issue with the service binding.

Retry may succeed.

 Value: 9

### RESULT_INVALID_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_INVALID_REQUEST: Int
```

Request object is not valid.

Retry not advised with current parameters.

 Value: 8

### RESULT_OK

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_OK: Int
```

Request is successful and the value was set.

 Value: 0

### RESULT_REQUIRE_APP_PERMISSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_REQUIRE_APP_PERMISSION: Int
```

Requested preference requires permissions not held by the calling application.

Retry may succeed if necessary permissions are obtained.

 Value: 5

### RESULT_REQUIRE_USER_CONSENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_REQUIRE_USER_CONSENT: Int
```

User consent was not approved for this operation.

Retry may succeed if user provides consent.

 Value: 6

### RESULT_RESTRICTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_RESTRICTED: Int
```

Requested preference is restricted, thus unable to be set under this policy.

Retry may succeed if underlying conditions change.

 Value: 3

### RESULT_UNAVAILABLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_UNAVAILABLE: Int
```

Preference is currently not available, likely due to device state or the state of a dependency.

Retry may succeed if underlying conditions change.

 Value: 4

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

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getResultCode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getResultCode(): Int
```

Returns the result code indicating status of the request.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_OK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_UNSUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_UNAVAILABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_REQUIRE_APP_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_REQUIRE_USER_CONSENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_DISALLOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_INVALID_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#RESULT_INTERNAL_ERROR:kotlin.Int` |

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
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SetValueResult!>
```

Parcelable Creator for `https://developer.android.com/reference/kotlin/android/service/settings/preferences/SetValueResult#`.
