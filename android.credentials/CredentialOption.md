# CredentialOption

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CredentialOption

Kotlin| [Java](https://developer.android.com/reference/android/credentials/CredentialOption "View this page in Java") 
| --- | --- |

```
class CredentialOption : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.credentials.CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#) |

Information about a specific type of credential to be requested during a android.credentials.CredentialManager#getCredential operation.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption.Builder) A builder for [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#). |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUPPORTED_ELEMENT_KEYS](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#SUPPORTED_ELEMENT_KEYS:kotlin.String) Bundle key to the list of elements keys supported/requested. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#describeContents())`()` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!\> | [getAllowedProviders](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#getAllowedProviders())`()` Returns the set of [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) corresponding to providers that must receive this option. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getCandidateQueryData](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#getCandidateQueryData())`()` Returns the partial request data that will be sent to the provider during the initial credential candidate query stage. |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getCredentialRetrievalData](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#getCredentialRetrievalData())`()` Returns the full request data. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#getType())`()` Returns the requested credential type. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemProviderRequired](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#isSystemProviderRequired())`()` Returns true if the request must only be fulfilled by a system provider, and false otherwise. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CredentialOption](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### SUPPORTED_ELEMENT_KEYS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPPORTED_ELEMENT_KEYS: String
```

Bundle key to the list of elements keys supported/requested. Framework will use this key to determine which types of Credentials will utilize Credential Registry when filtering Credential Providers to ping. 

 Value: "android.credentials.GetCredentialOption.SUPPORTED_ELEMENT_KEYS"

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAllowedProviders

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAllowedProviders(): MutableSet<ComponentName!>
```

Returns the set of [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) corresponding to providers that must receive this option.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!> | This value cannot be`null`. |

### getCandidateQueryData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCandidateQueryData(): Bundle
```

Returns the partial request data that will be sent to the provider during the initial credential candidate query stage. For security reason, a provider will receive the request data in two stages. First it gets this partial request that do not contain sensitive user information; it uses this information to provide credential candidates that the \[@code CredentialManager\] will show to the user. Next, the full request data, [getCredentialRetrievalData()](https://developer.android.com/reference/kotlin/android/credentials/CredentialOption#getCredentialRetrievalData()), will be sent to a provider only if the user further grants the consent by choosing a candidate from the provider.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getCredentialRetrievalData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialRetrievalData(): Bundle
```

Returns the full request data.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String
```

Returns the requested credential type.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### isSystemProviderRequired

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSystemProviderRequired(): Boolean
```

Returns true if the request must only be fulfilled by a system provider, and false otherwise. 

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
static val CREATOR: Parcelable.Creator<CredentialOption!>
```
