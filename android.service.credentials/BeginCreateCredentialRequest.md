Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BeginCreateCredentialRequest

Kotlin | [Java](BeginCreateCredentialRequest.md)
| --- | --- |

```
class BeginCreateCredentialRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.BeginCreateCredentialRequest](BeginCreateCredentialRequest.md) |

Request for beginning a create credential request. See `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialResponse` for the counterpart response

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#BeginCreateCredentialRequest(kotlin.String,%20android.os.Bundle)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, data: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Constructs a new instance without `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo`. |
| `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#BeginCreateCredentialRequest(kotlin.String,%20android.os.Bundle,%20android.service.credentials.CallingAppInfo)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, data: https://developer.android.com/reference/kotlin/android/os/Bundle.html#, callingAppInfo: https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo?)` Constructs a new instance. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [CallingAppInfo](CallingAppInfo.md)? | `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#getCallingAppInfo()()` Returns the info pertaining to the calling app. |
| [Bundle](../android.os/Bundle.md) | `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#getData()()` Returns the data to be used while resolving the credential to create. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#getType()()` Returns the type of the credential to be created. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BeginCreateCredentialRequest](BeginCreateCredentialRequest.md)!\> | `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### BeginCreateCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BeginCreateCredentialRequest(
    type: String, 
    data: Bundle)
```

Constructs a new instance without `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo`.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `data` | [Bundle](../android.os/Bundle.md): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If {`type` string is null or empty. |
| `java.lang.NullPointerException` | If `data` is null. |

### BeginCreateCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
BeginCreateCredentialRequest(
    type: String, 
    data: Bundle, 
    callingAppInfo: CallingAppInfo?)
```

Constructs a new instance.

| Parameters ||
|---|---|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `data` | [Bundle](../android.os/Bundle.md): This value cannot be `null`. |
| `callingAppInfo` | [CallingAppInfo](CallingAppInfo.md)?: This value may be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `callingAppInfo`, or `type` string is null or empty. |
| `java.lang.NullPointerException` | If `data` is null. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getCallingAppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCallingAppInfo(): CallingAppInfo?
```

Returns the info pertaining to the calling app. This value can be null when this instance is set on a `https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest` or a `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialRequest#` if the caller of the API does not wish to propagate this information to a credential provider.

### getData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getData(): Bundle
```

Returns the data to be used while resolving the credential to create.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | This value cannot be `null`. |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): String
```

Returns the type of the credential to be created.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<BeginCreateCredentialRequest!>
```
