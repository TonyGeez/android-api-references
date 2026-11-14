Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallingAppInfo

Kotlin | [Java](../android/service/credentials/CallingAppInfo.md)
| --- | --- |

```
class CallingAppInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.CallingAppInfo](../android/service/credentials/CallingAppInfo.md) |

Information pertaining to the calling application, including the package name and a list of app signatures.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#CallingAppInfo(kotlin.String,%20android.content.pm.SigningInfo)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, signingInfo: https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo.html#)` Constructs a new instance. |
| `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#CallingAppInfo(kotlin.String,%20android.content.pm.SigningInfo,%20kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, signingInfo: https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo.html#, origin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Constructs a new instance. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#getOrigin()()` Returns the origin of the calling app if set otherwise returns null. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#getPackageName()()` Returns the package name of the source of this info. |
| --- | --- |
| [SigningInfo](../android/content/pm/SigningInfo.md) | `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#getSigningInfo()()` Returns the SigningInfo object that contains an array of `https://developer.android.com/reference/kotlin/android/content/pm/Signature.html#` belonging to the app. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CallingAppInfo](../android/service/credentials/CallingAppInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### CallingAppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CallingAppInfo(
    packageName: String, 
    signingInfo: SigningInfo)
```

Constructs a new instance.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `signingInfo` | [SigningInfo](../android/content/pm/SigningInfo.md): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `packageName` is null or empty. |
| `java.lang.NullPointerException` | If `signingInfo` is null. |

### CallingAppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CallingAppInfo(
    packageName: String, 
    signingInfo: SigningInfo, 
    origin: String?)
```

Constructs a new instance.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): - the package name of the calling app. This value cannot be `null`. |
| `signingInfo` | [SigningInfo](../android/content/pm/SigningInfo.md): - the signing info on the calling app. This value cannot be `null`. |
| `origin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: - the origin that the calling app wants to use when making request on behalf of other. This value may be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If `packageName` is null or empty. |
| `java.lang.NullPointerException` | If `signingInfo` is null. |

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

### getOrigin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOrigin(): String?
```

Returns the origin of the calling app if set otherwise returns null. This value is set only if the origin is different than that of the calling app, and should be expected from privileged callers(browsers) only when making request on behalf of other applications. Android system makes sure that only applications that poses the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CREDENTIAL_MANAGER_SET_ORIGIN:kotlin.String` can set the origin on the incoming `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#` or `https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest.html#`.

### getPackageName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String
```

Returns the package name of the source of this info.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getSigningInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSigningInfo(): SigningInfo
```

Returns the SigningInfo object that contains an array of `https://developer.android.com/reference/kotlin/android/content/pm/Signature.html#` belonging to the app.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/SigningInfo.html#` | This value cannot be `null`. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

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
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CallingAppInfo!>
```
