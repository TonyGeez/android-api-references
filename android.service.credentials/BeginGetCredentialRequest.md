# BeginGetCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BeginGetCredentialRequest

Kotlin| [Java](BeginGetCredentialRequest.md) 
| --- | --- |

```
class BeginGetCredentialRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.BeginGetCredentialRequest](BeginGetCredentialRequest.md) |

Query stage request for getting user's credentials from a given credential provider.

This request contains a list of [BeginGetCredentialOption](BeginGetCredentialOption.md) that have parameters to be used to query credentials, and return a list of [CredentialEntry](CredentialEntry.md) to be set on the [BeginGetCredentialResponse](BeginGetCredentialResponse.md). This list is then shown to the user on a selector. If a [PendingIntent](../android.app/PendingIntent.md) is set on a [CredentialEntry](CredentialEntry.md), and the user selects that entry, a [GetCredentialRequest](GetCredentialRequest.md) with all parameters needed to get the actual [android.credentials.Credential](../android.credentials/Credential.md) will be sent as part of the [Intent](../android.content/Intent.md) fired through the [PendingIntent](../android.app/PendingIntent.md).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/credentials/BeginGetCredentialRequest.Builder.md) Builder for [BeginGetCredentialRequest](BeginGetCredentialRequest.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](BeginGetCredentialRequest.md))`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BeginGetCredentialOption](BeginGetCredentialOption.md)!\> | [getBeginGetCredentialOptions](BeginGetCredentialRequest.md))`()` Returns the list of type specific credential options to list credentials for in [BeginGetCredentialResponse](BeginGetCredentialResponse.md). |
| [CallingAppInfo](CallingAppInfo.md)? | [getCallingAppInfo](BeginGetCredentialRequest.md))`()` Returns info pertaining to the app requesting credentials. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](BeginGetCredentialRequest.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BeginGetCredentialRequest](BeginGetCredentialRequest.md)!\> | [CREATOR](BeginGetCredentialRequest.md) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getBeginGetCredentialOptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBeginGetCredentialOptions(): MutableList<BeginGetCredentialOption!>
```

Returns the list of type specific credential options to list credentials for in [BeginGetCredentialResponse](BeginGetCredentialResponse.md).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BeginGetCredentialOption](BeginGetCredentialOption.md)!> | This value cannot be`null`. |

### getCallingAppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingAppInfo(): CallingAppInfo?
```

Returns info pertaining to the app requesting credentials.

| Return ||
|--------------------------------------------------------------------------------------------------------------|--------------------------|
| [CallingAppInfo](CallingAppInfo.md)? | This value may be`null`. |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BeginGetCredentialRequest!>
```
