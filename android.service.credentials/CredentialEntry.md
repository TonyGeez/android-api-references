# CredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialEntry

Kotlin| [Java](../android/service/credentials/CredentialEntry.md) 
| --- | --- |

```
class CredentialEntry : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.CredentialEntry](../android/service/credentials/CredentialEntry.md) |

A credential entry that is to be displayed on the account selector that is presented to the user.

If user selects this entry, the corresponding [PendingIntent](../android/app/PendingIntent.md), set on the`slice`will be invoked to launch activities that require some user engagement before getting the credential corresponding to this entry, e.g. authentication, confirmation etc. The extras associated with the resulting [android.app.Activity](../android/app/Activity.md) will also contain the complete credential request containing all required parameters. This request can be retrieved against [CredentialProviderService.EXTRA_GET_CREDENTIAL_REQUEST](../android/service/credentials/CredentialProviderService.md). Once the activity fulfills the required user engagement, the [android.app.Activity](../android/app/Activity.md) result should be set to [android.app.Activity#RESULT_OK](../android/app/Activity.md), and the [CredentialProviderService.EXTRA_GET_CREDENTIAL_RESPONSE](../android/service/credentials/CredentialProviderService.md) must be set with a [GetCredentialResponse](../android/credentials/GetCredentialResponse.md) object.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CredentialEntry](../android/service/credentials/CredentialEntry.md))`(`beginGetCredentialOption:` ` [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md)`, `slice:` ` [Slice](../android/app/slice/Slice.md)`)` Creates an entry that is associated with a [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) request. |
| [CredentialEntry](../android/service/credentials/CredentialEntry.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `slice:` ` [Slice](../android/app/slice/Slice.md)`)` Creates an entry that is independent of an incoming [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) request. |
| [CredentialEntry](../android/service/credentials/CredentialEntry.md))`(`beginGetCredentialOptionId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `slice:` ` [Slice](../android/app/slice/Slice.md)`)` Creates an entry that is associated with a [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) request. |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/credentials/CredentialEntry.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getBeginGetCredentialOptionId](../android/service/credentials/CredentialEntry.md))`()` Returns the id of the [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) for which this credential entry has been constructed. |
| [Slice](../android/app/slice/Slice.md) | [getSlice](../android/service/credentials/CredentialEntry.md))`()` Returns the [Slice](../android/app/slice/Slice.md) object containing UI display content to be shown for this entry. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](../android/service/credentials/CredentialEntry.md))`()` Returns the specific credential type of the entry. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/credentials/CredentialEntry.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CredentialEntry](../android/service/credentials/CredentialEntry.md)!\> | [CREATOR](../android/service/credentials/CredentialEntry.md) <br /> |

## Public constructors

### CredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CredentialEntry(
    beginGetCredentialOption: BeginGetCredentialOption, 
    slice: Slice)
```

Creates an entry that is associated with a [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) request. Providers must use this constructor when they extend from [CredentialProviderService](../android/service/credentials/CredentialProviderService.md) to respond to query phase [CredentialProviderService.onBeginGetCredential](../android/service/credentials/CredentialProviderService.md))credential retrieval requests.

| Parameters ||
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `beginGetCredentialOption` | [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md):the request option for which this credential entry is being constructed This helps maintain an association, such that when the user selects this entry, providers can receive the complete corresponding request. This value cannot be`null`. |
| `slice` | [Slice](../android/app/slice/Slice.md):the slice containing the metadata to be shown on the UI. Must be constructed through the androidx.credentials jetpack library. This value cannot be`null`. |

### CredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CredentialEntry(
    type: String, 
    slice: Slice)
```

Creates an entry that is independent of an incoming [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) request. Providers must use this constructor for constructing entries to be registered with the framework outside of the span of an API call.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the type of the credential This value cannot be`null`. |
| `slice` | [Slice](../android/app/slice/Slice.md):the slice containing the metadata to be shown on the UI. Must be constructed through the androidx.credentials jetpack library. This value cannot be`null`. |

### CredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CredentialEntry(
    beginGetCredentialOptionId: String, 
    type: String, 
    slice: Slice)
```

Creates an entry that is associated with a [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) request. Providers must use this constructor when they extend from [CredentialProviderService](../android/service/credentials/CredentialProviderService.md) to respond to query phase [CredentialProviderService.onBeginGetCredential](../android/service/credentials/CredentialProviderService.md))credential retrieval requests.

| Parameters ||
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `beginGetCredentialOptionId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the beginGetCredentialOptionId to be retrieved from [BeginGetCredentialOption.getId()](../android/service/credentials/BeginGetCredentialOption.md))- the request option for which this CredentialEntry is being constructed This helps maintain an association such that when the user selects this entry, providers can receive the complete corresponding [GetCredentialRequest](../android/service/credentials/GetCredentialRequest.md). This value cannot be`null`. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the type of the credential for which this credential entry is being created This value cannot be`null`. |
| `slice` | [Slice](../android/app/slice/Slice.md):the slice containing the metadata to be shown on the UI, must be constructed through the androidx.credentials.provider Jetpack library; If constructed manually, the`slice`object must contain the non-null properties of the androidx.credentials.provider.CredentialEntry class populated as slice items against specific hints as used in the class's`toSlice`method, since the Android System uses this library to parse the`slice`and extract the required attributes |
| --- | --- |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getBeginGetCredentialOptionId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBeginGetCredentialOptionId(): String
```

Returns the id of the [BeginGetCredentialOption](../android/service/credentials/BeginGetCredentialOption.md) for which this credential entry has been constructed.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getSlice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlice(): Slice
```

Returns the [Slice](../android/app/slice/Slice.md) object containing UI display content to be shown for this entry.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [Slice](../android/app/slice/Slice.md) | This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CredentialEntry!>
```
