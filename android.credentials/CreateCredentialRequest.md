# CreateCredentialRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CreateCredentialRequest

Kotlin| [Java](../android/credentials/CreateCredentialRequest.md) 
| --- | --- |

```
class CreateCredentialRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.credentials.CreateCredentialRequest](../android/credentials/CreateCredentialRequest.md) |

A request to register a specific type of user credential, potentially launching UI flows to collect user consent and any other operation needed.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/credentials/CreateCredentialRequest.Builder.md) A builder for [CreateCredentialRequest](../android/credentials/CreateCredentialRequest.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [alwaysSendAppInfoToProvider](../android/credentials/CreateCredentialRequest.md))`()` Return true/false value to determine if the calling app info should always be sent to providers (if true), or removed from the query phase (if false). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/credentials/CreateCredentialRequest.md))`()` <br /> |
| [Bundle](../android/os/Bundle.md) | [getCandidateQueryData](../android/credentials/CreateCredentialRequest.md))`()` Returns the partial request data that will be sent to the provider during the initial creation candidate query stage. |
| --- | --- |
| [Bundle](../android/os/Bundle.md) | [getCredentialData](../android/credentials/CreateCredentialRequest.md))`()` Returns the full credential creation request data. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getOrigin](../android/credentials/CreateCredentialRequest.md))`()` Returns the origin of the calling app if set otherwise returns null. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](../android/credentials/CreateCredentialRequest.md))`()` Returns the requested credential type. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSystemProviderRequired](../android/credentials/CreateCredentialRequest.md))`()` Returns true if the request must only be fulfilled by a system provider, and false otherwise. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/credentials/CreateCredentialRequest.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/credentials/CreateCredentialRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CreateCredentialRequest](../android/credentials/CreateCredentialRequest.md)!\> | [CREATOR](../android/credentials/CreateCredentialRequest.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCandidateQueryData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCandidateQueryData(): Bundle
```

Returns the partial request data that will be sent to the provider during the initial creation candidate query stage. For security reason, a provider will receive the request data in two stages. First it gets this partial request that do not contain sensitive user information; it uses this information to provide credential creation candidates that the \[@code CredentialManager\] will show to the user. Next, the full request data, [getCredentialData()](../android/credentials/CreateCredentialRequest.md)), will be sent to a provider only if the user further grants the consent by choosing a candidate from the provider.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](../android/os/Bundle.md) | This value cannot be`null`. |

### getCredentialData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialData(): Bundle
```

Returns the full credential creation request data. For security reason, a provider will receive the request data in two stages. First it gets a partial request, [getCandidateQueryData()](../android/credentials/CreateCredentialRequest.md))that do not contain sensitive user information; it uses this information to provide credential creation candidates that the \[@code CredentialManager\] will show to the user. Next, this full request data will be sent to a provider only if the user further grants the consent by choosing a candidate from the provider.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](../android/os/Bundle.md) | This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CreateCredentialRequest!>
```
