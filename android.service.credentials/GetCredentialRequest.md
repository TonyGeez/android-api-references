# GetCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetCredentialRequest

Kotlin| [Java](https://developer.android.com/reference/android/service/credentials/GetCredentialRequest "View this page in Java") 
| --- | --- |

```
class GetCredentialRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.GetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#) |

Request for getting user's credential from a given credential provider.

A credential provider will receive this request once the user selects a given [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry), or [RemoteEntry](https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry) on the selector, that was sourced from provider's initial response to [CredentialProviderService.onBeginGetCredential](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#onBeginGetCredential(android.service.credentials.BeginGetCredentialRequest,%20android.os.CancellationSignal,%20android.os.OutcomeReceiver)).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#GetCredentialRequest(android.service.credentials.CallingAppInfo,%20kotlin.collections.MutableList))`(`callingAppInfo:` ` [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo)`, `credentialOptions:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption.html#)!>`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#describeContents())`()` <br /> |
| [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo) | [getCallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#getCallingAppInfo())`()` Returns info pertaining to the app requesting credentials. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption.html#)!\> | [getCredentialOptions](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#getCredentialOptions())`()` Returns a list of options containing parameters needed to return a given type of credential. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### GetCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GetCredentialRequest(
    callingAppInfo: CallingAppInfo, 
    credentialOptions: MutableList<CredentialOption!>)
```

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callingAppInfo` | [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo):This value cannot be`null`. |
| `credentialOptions` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption.html#)!\>:This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCallingAppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingAppInfo(): CallingAppInfo
```

Returns info pertaining to the app requesting credentials.

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo) | This value cannot be`null`. |

### getCredentialOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialOptions(): MutableList<CredentialOption!>
```

Returns a list of options containing parameters needed to return a given type of credential. This is part of the request that the credential provider receives after the user has selected an entry on a selector UI. When the user selects a [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry) and the credential provider receives a [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#), this list is expected to contain a single [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption.html#) only. A [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry) is always created for a given [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption), and hence when the user selects it, the provider receives a corresponding [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption.html#) that contains all the required parameters to actually retrieve the credential. When the user selects a [RemoteEntry](https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry) and the credential provider receives a [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest#), this list may contain greater than a single [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption.html#), representing the number of options specified by the developer in the original [android.credentials.GetCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialRequest.html#). This is because a [RemoteEntry](https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry) indicates that the entire request will be processed on a different device and is not tied to a particular option.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption.html#)!> | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<GetCredentialRequest!>
```
