# BeginGetCredentialResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BeginGetCredentialResponse

Kotlin| [Java](../android/service/credentials/BeginGetCredentialResponse.md) 
| --- | --- |

```
class BeginGetCredentialResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.BeginGetCredentialResponse](../android/service/credentials/BeginGetCredentialResponse.md) |

Response from a credential provider, containing credential entries and other associated data to be shown on the account selector UI.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/service/credentials/BeginGetCredentialResponse.Builder.md) Builds an instance of [BeginGetCredentialResponse](../android/service/credentials/BeginGetCredentialResponse.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BeginGetCredentialResponse](../android/service/credentials/BeginGetCredentialResponse.md))`()` Creates an empty response instance, to be used when there are no [CredentialEntry](../android/service/credentials/CredentialEntry.md), or [Action](../android/service/credentials/Action.md) to return. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/service/credentials/BeginGetCredentialResponse.md))`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Action](../android/service/credentials/Action.md)!\> | [getActions](../android/service/credentials/BeginGetCredentialResponse.md))`()` Returns the list of actions to be displayed on the UI. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Action](../android/service/credentials/Action.md)!\> | [getAuthenticationActions](../android/service/credentials/BeginGetCredentialResponse.md))`()` Returns the list of authentication entries to be displayed on the UI. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CredentialEntry](../android/service/credentials/CredentialEntry.md)!\> | [getCredentialEntries](../android/service/credentials/BeginGetCredentialResponse.md))`()` Returns the list of credential entries to be displayed on the UI. |
| [RemoteEntry](../android/service/credentials/RemoteEntry.md)? | [getRemoteCredentialEntry](../android/service/credentials/BeginGetCredentialResponse.md))`()` Returns the remote credential entry to be displayed on the UI. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/service/credentials/BeginGetCredentialResponse.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BeginGetCredentialResponse](../android/service/credentials/BeginGetCredentialResponse.md)!\> | [CREATOR](../android/service/credentials/BeginGetCredentialResponse.md) <br /> |

## Public constructors

### BeginGetCredentialResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BeginGetCredentialResponse()
```

Creates an empty response instance, to be used when there are no [CredentialEntry](../android/service/credentials/CredentialEntry.md), or [Action](../android/service/credentials/Action.md) to return.

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getActions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActions(): MutableList<Action!>
```

Returns the list of actions to be displayed on the UI.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Action](../android/service/credentials/Action.md)!> | This value cannot be`null`. |

### getAuthenticationActions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAuthenticationActions(): MutableList<Action!>
```

Returns the list of authentication entries to be displayed on the UI.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Action](../android/service/credentials/Action.md)!> | This value cannot be`null`. |

### getCredentialEntries

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialEntries(): MutableList<CredentialEntry!>
```

Returns the list of credential entries to be displayed on the UI.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CredentialEntry](../android/service/credentials/CredentialEntry.md)!> | This value cannot be`null`. |

### getRemoteCredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteCredentialEntry(): RemoteEntry?
```

Returns the remote credential entry to be displayed on the UI.

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------|
| [RemoteEntry](../android/service/credentials/RemoteEntry.md)? | This value may be`null`. |

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
static val CREATOR: Parcelable.Creator<BeginGetCredentialResponse!>
```
