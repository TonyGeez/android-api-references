# BeginGetCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BeginGetCredentialRequest

Kotlin| [Java](https://developer.android.com/reference/android/service/credentials/BeginGetCredentialRequest "View this page in Java") 

```
class BeginGetCredentialRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.credentials.BeginGetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest#) |

Query stage request for getting user's credentials from a given credential provider.

This request contains a list of [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) that have parameters to be used to query credentials, and return a list of [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry) to be set on the [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse). This list is then shown to the user on a selector. If a [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) is set on a [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry), and the user selects that entry, a [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest) with all parameters needed to get the actual [android.credentials.Credential](https://developer.android.com/reference/kotlin/android/credentials/Credential.html#) will be sent as part of the [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) fired through the [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest.Builder) Builder for [BeginGetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption)!\> | [getBeginGetCredentialOptions](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest#getBeginGetCredentialOptions())`()` Returns the list of type specific credential options to list credentials for in [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse). |
| [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo)? | [getCallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest#getCallingAppInfo())`()` Returns info pertaining to the app requesting credentials. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BeginGetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getBeginGetCredentialOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBeginGetCredentialOptions(): MutableList<BeginGetCredentialOption!>
```

Returns the list of type specific credential options to list credentials for in [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption)!> | This value cannot be`null`. |

### getCallingAppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingAppInfo(): CallingAppInfo?
```

Returns info pertaining to the app requesting credentials.

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------------|
| [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo)? | This value may be`null`. |

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BeginGetCredentialRequest!>
```
