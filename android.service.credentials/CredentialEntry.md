# CredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialEntry

Kotlin| [Java](https://developer.android.com/reference/android/service/credentials/CredentialEntry "View this page in Java") 

```
class CredentialEntry : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.credentials.CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#) |

A credential entry that is to be displayed on the account selector that is presented to the user.

If user selects this entry, the corresponding [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#), set on the`slice`will be invoked to launch activities that require some user engagement before getting the credential corresponding to this entry, e.g. authentication, confirmation etc. The extras associated with the resulting [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) will also contain the complete credential request containing all required parameters. This request can be retrieved against [CredentialProviderService.EXTRA_GET_CREDENTIAL_REQUEST](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#EXTRA_GET_CREDENTIAL_REQUEST:kotlin.String). Once the activity fulfills the required user engagement, the [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) result should be set to [android.app.Activity#RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int), and the [CredentialProviderService.EXTRA_GET_CREDENTIAL_RESPONSE](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#EXTRA_GET_CREDENTIAL_RESPONSE:kotlin.String) must be set with a [GetCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#) object.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#CredentialEntry(android.service.credentials.BeginGetCredentialOption,%20android.app.slice.Slice))`(`beginGetCredentialOption:` ` [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption)`, `slice:` ` [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#)`)` Creates an entry that is associated with a [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) request. |
| [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#CredentialEntry(kotlin.String,%20android.app.slice.Slice))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `slice:` ` [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#)`)` Creates an entry that is independent of an incoming [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) request. |
| [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#CredentialEntry(kotlin.String,%20kotlin.String,%20android.app.slice.Slice))`(`beginGetCredentialOptionId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `slice:` ` [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#)`)` Creates an entry that is associated with a [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) request. |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#describeContents())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getBeginGetCredentialOptionId](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#getBeginGetCredentialOptionId())`()` Returns the id of the [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) for which this credential entry has been constructed. |
| [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) | [getSlice](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#getSlice())`()` Returns the [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) object containing UI display content to be shown for this entry. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#getType())`()` Returns the specific credential type of the entry. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### CredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CredentialEntry(
    beginGetCredentialOption: BeginGetCredentialOption, 
    slice: Slice)
```

Creates an entry that is associated with a [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) request. Providers must use this constructor when they extend from [CredentialProviderService](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService) to respond to query phase [CredentialProviderService.onBeginGetCredential](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#onBeginGetCredential(android.service.credentials.BeginGetCredentialRequest,%20android.os.CancellationSignal,%20android.os.OutcomeReceiver))credential retrieval requests.

| Parameters ||
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `beginGetCredentialOption` | [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption):the request option for which this credential entry is being constructed This helps maintain an association, such that when the user selects this entry, providers can receive the complete corresponding request. This value cannot be`null`. |
| `slice` | [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#):the slice containing the metadata to be shown on the UI. Must be constructed through the androidx.credentials jetpack library. This value cannot be`null`. |

### CredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CredentialEntry(
    type: String, 
    slice: Slice)
```

Creates an entry that is independent of an incoming [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) request. Providers must use this constructor for constructing entries to be registered with the framework outside of the span of an API call.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the type of the credential This value cannot be`null`. |
| `slice` | [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#):the slice containing the metadata to be shown on the UI. Must be constructed through the androidx.credentials jetpack library. This value cannot be`null`. |

### CredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CredentialEntry(
    beginGetCredentialOptionId: String, 
    type: String, 
    slice: Slice)
```

Creates an entry that is associated with a [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) request. Providers must use this constructor when they extend from [CredentialProviderService](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService) to respond to query phase [CredentialProviderService.onBeginGetCredential](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#onBeginGetCredential(android.service.credentials.BeginGetCredentialRequest,%20android.os.CancellationSignal,%20android.os.OutcomeReceiver))credential retrieval requests.

| Parameters ||
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `beginGetCredentialOptionId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the beginGetCredentialOptionId to be retrieved from [BeginGetCredentialOption.getId()](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#getId())- the request option for which this CredentialEntry is being constructed This helps maintain an association such that when the user selects this entry, providers can receive the complete corresponding [GetCredentialRequest](https://developer.android.com/reference/kotlin/android/service/credentials/GetCredentialRequest). This value cannot be`null`. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the type of the credential for which this credential entry is being created This value cannot be`null`. |
| `slice` | [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#):the slice containing the metadata to be shown on the UI, must be constructed through the androidx.credentials.provider Jetpack library; If constructed manually, the`slice`object must contain the non-null properties of the androidx.credentials.provider.CredentialEntry class populated as slice items against specific hints as used in the class's`toSlice`method, since the Android System uses this library to parse the`slice`and extract the required attributes |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If`beginGetCredentialOptionId`or`type`is null, or empty |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getBeginGetCredentialOptionId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBeginGetCredentialOptionId(): String
```

Returns the id of the [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption) for which this credential entry has been constructed.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getSlice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlice(): Slice
```

Returns the [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) object containing UI display content to be shown for this entry.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) | This value cannot be`null`. |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String
```

Returns the specific credential type of the entry.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<CredentialEntry!>
```
