# CreateCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CreateCredentialRequest

Kotlin| [Java](https://developer.android.com/reference/android/credentials/CreateCredentialRequest "View this page in Java") 
| --- | --- |

```
class CreateCredentialRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.credentials.CreateCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#) |

A request to register a specific type of user credential, potentially launching UI flows to collect user consent and any other operation needed.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest.Builder) A builder for [CreateCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [alwaysSendAppInfoToProvider](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#alwaysSendAppInfoToProvider())`()` Return true/false value to determine if the calling app info should always be sent to providers (if true), or removed from the query phase (if false). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#describeContents())`()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getCandidateQueryData](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#getCandidateQueryData())`()` Returns the partial request data that will be sent to the provider during the initial creation candidate query stage. |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getCredentialData](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#getCredentialData())`()` Returns the full credential creation request data. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getOrigin](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#getOrigin())`()` Returns the origin of the calling app if set otherwise returns null. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#getType())`()` Returns the requested credential type. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemProviderRequired](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#isSystemProviderRequired())`()` Returns true if the request must only be fulfilled by a system provider, and false otherwise. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CreateCredentialRequest](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### alwaysSendAppInfoToProvider

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun alwaysSendAppInfoToProvider(): Boolean
```

Return true/false value to determine if the calling app info should always be sent to providers (if true), or removed from the query phase (if false). 

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCandidateQueryData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCandidateQueryData(): Bundle
```

Returns the partial request data that will be sent to the provider during the initial creation candidate query stage. For security reason, a provider will receive the request data in two stages. First it gets this partial request that do not contain sensitive user information; it uses this information to provide credential creation candidates that the \[@code CredentialManager\] will show to the user. Next, the full request data, [getCredentialData()](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#getCredentialData()), will be sent to a provider only if the user further grants the consent by choosing a candidate from the provider.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getCredentialData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialData(): Bundle
```

Returns the full credential creation request data. For security reason, a provider will receive the request data in two stages. First it gets a partial request, [getCandidateQueryData()](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialRequest#getCandidateQueryData())that do not contain sensitive user information; it uses this information to provide credential creation candidates that the \[@code CredentialManager\] will show to the user. Next, this full request data will be sent to a provider only if the user further grants the consent by choosing a candidate from the provider.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getOrigin

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOrigin(): String?
```

Returns the origin of the calling app if set otherwise returns null. 

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
static val CREATOR: Parcelable.Creator<CreateCredentialRequest!>
```
