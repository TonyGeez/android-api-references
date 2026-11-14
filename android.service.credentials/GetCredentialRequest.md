# GetCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetCredentialRequest

Kotlin| [Java](../android/service/credentials/GetCredentialRequest.md) 
| --- | --- |

```
class GetCredentialRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.GetCredentialRequest](../android/service/credentials/GetCredentialRequest.md) |

Request for getting user's credential from a given credential provider.

A credential provider will receive this request once the user selects a given [CredentialEntry](../android/service/credentials/CredentialEntry.md), or [RemoteEntry](../android/service/credentials/RemoteEntry.md) on the selector, that was sourced from provider's initial response to [CredentialProviderService.onBeginGetCredential](../android/service/credentials/CredentialProviderService.md)).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GetCredentialRequest](../android/service/credentials/GetCredentialRequest.md))`(`callingAppInfo:` ` [CallingAppInfo](../android/service/credentials/CallingAppInfo.md)`, `credentialOptions:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CredentialOption](../android/credentials/CredentialOption.md)!>`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/credentials/GetCredentialRequest.md))`()` <br /> |
| [CallingAppInfo](../android/service/credentials/CallingAppInfo.md) | [getCallingAppInfo](../android/service/credentials/GetCredentialRequest.md))`()` Returns info pertaining to the app requesting credentials. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CredentialOption](../android/credentials/CredentialOption.md)!\> | [getCredentialOptions](../android/service/credentials/GetCredentialRequest.md))`()` Returns a list of options containing parameters needed to return a given type of credential. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/credentials/GetCredentialRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [GetCredentialRequest](../android/service/credentials/GetCredentialRequest.md)!\> | [CREATOR](../android/service/credentials/GetCredentialRequest.md) <br /> |

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
| `callingAppInfo` | [CallingAppInfo](../android/service/credentials/CallingAppInfo.md):This value cannot be`null`. |
| `credentialOptions` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CredentialOption](../android/credentials/CredentialOption.md)!\>:This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCallingAppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingAppInfo(): CallingAppInfo
```

Returns info pertaining to the app requesting credentials.

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [CallingAppInfo](../android/service/credentials/CallingAppInfo.md) | This value cannot be`null`. |

### getCredentialOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialOptions(): MutableList<CredentialOption!>
```

Returns a list of options containing parameters needed to return a given type of credential. This is part of the request that the credential provider receives after the user has selected an entry on a selector UI. When the user selects a [CredentialEntry](../android/service/credentials/CredentialEntry.md) and the credential provider receives a [GetCredentialRequest](../android/service/credentials/GetCredentialRequest.md), this list is expected to contain a single [CredentialOption](../android/credentials/CredentialOption.md) only. A [CredentialEntry](../android/service/credentials/CredentialEntry.md) is always created for a given [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md), and hence when the user selects it, the provider receives a corresponding [CredentialOption](../android/credentials/CredentialOption.md) that contains all the required parameters to actually retrieve the credential. When the user selects a [RemoteEntry](../android/service/credentials/RemoteEntry.md) and the credential provider receives a [GetCredentialRequest](../android/service/credentials/GetCredentialRequest.md), this list may contain greater than a single [CredentialOption](../android/credentials/CredentialOption.md), representing the number of options specified by the developer in the original [android.credentials.GetCredentialRequest](../android/credentials/GetCredentialRequest.md). This is because a [RemoteEntry](../android/service/credentials/RemoteEntry.md) indicates that the entire request will be processed on a different device and is not tied to a particular option.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CredentialOption](../android/credentials/CredentialOption.md)!> | This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<GetCredentialRequest!>
```
