# BeginGetCredentialResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BeginGetCredentialResponse

Kotlin| [Java](https://developer.android.com/reference/android/service/credentials/BeginGetCredentialResponse "View this page in Java") 

```
class BeginGetCredentialResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.credentials.BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#) |

Response from a credential provider, containing credential entries and other associated data to be shown on the account selector UI.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse.Builder) Builds an instance of [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#BeginGetCredentialResponse())`()` Creates an empty response instance, to be used when there are no [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry), or [Action](https://developer.android.com/reference/kotlin/android/service/credentials/Action) to return. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Action](https://developer.android.com/reference/kotlin/android/service/credentials/Action)!\> | [getActions](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#getActions())`()` Returns the list of actions to be displayed on the UI. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Action](https://developer.android.com/reference/kotlin/android/service/credentials/Action)!\> | [getAuthenticationActions](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#getAuthenticationActions())`()` Returns the list of authentication entries to be displayed on the UI. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry)!\> | [getCredentialEntries](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#getCredentialEntries())`()` Returns the list of credential entries to be displayed on the UI. |
| [RemoteEntry](https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry)? | [getRemoteCredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#getRemoteCredentialEntry())`()` Returns the remote credential entry to be displayed on the UI. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### BeginGetCredentialResponse

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BeginGetCredentialResponse()
```

Creates an empty response instance, to be used when there are no [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry), or [Action](https://developer.android.com/reference/kotlin/android/service/credentials/Action) to return.

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getActions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActions(): MutableList<Action!>
```

Returns the list of actions to be displayed on the UI.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Action](https://developer.android.com/reference/kotlin/android/service/credentials/Action)!> | This value cannot be`null`. |

### getAuthenticationActions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAuthenticationActions(): MutableList<Action!>
```

Returns the list of authentication entries to be displayed on the UI.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Action](https://developer.android.com/reference/kotlin/android/service/credentials/Action)!> | This value cannot be`null`. |

### getCredentialEntries

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialEntries(): MutableList<CredentialEntry!>
```

Returns the list of credential entries to be displayed on the UI.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry)!> | This value cannot be`null`. |

### getRemoteCredentialEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteCredentialEntry(): RemoteEntry?
```

Returns the remote credential entry to be displayed on the UI.

| Return ||
|--------------------------------------------------------------------------------------------------------|--------------------------|
| [RemoteEntry](https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry)? | This value may be`null`. |

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
static val CREATOR: Parcelable.Creator<BeginGetCredentialResponse!>
```
