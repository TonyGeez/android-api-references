# BeginGetCredentialOption

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BeginGetCredentialOption

Kotlin| [Java](https://developer.android.com/reference/android/service/credentials/BeginGetCredentialOption "View this page in Java") 
| --- | --- |

```
class BeginGetCredentialOption : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#) |

A specific type of credential request to be sent to the provider during the query phase of a get flow. This request contains limited parameters needed to populate a list of [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry) on the [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#BeginGetCredentialOption(kotlin.String,%20kotlin.String,%20android.os.Bundle))`(`id:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `candidateQueryData:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Constructs a [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#). |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#describeContents())`()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getCandidateQueryData](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#getCandidateQueryData())`()` Returns the request candidate query data, denoting a set of parameters that can be used to populate a candidate list of credentials, as [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry) on [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#getId())`()` Returns the unique id associated with this request. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#getType())`()` Returns the requested credential type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### BeginGetCredentialOption

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BeginGetCredentialOption(
    id: String, 
    type: String, 
    candidateQueryData: Bundle)
```

Constructs a [BeginGetCredentialOption](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialOption#).

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the unique id associated with this option This value cannot be`null`. |
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the requested credential type This value cannot be`null`. |
| `candidateQueryData` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):the request candidateQueryData This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | If id or type is empty. |

## Public methods

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

Returns the request candidate query data, denoting a set of parameters that can be used to populate a candidate list of credentials, as [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry) on [BeginGetCredentialResponse](https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse). This list of entries is then presented to the user on a selector.

This data does not contain any sensitive parameters, and will be sent to all eligible providers. The complete set of parameters will only be set on the [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) set on the [CredentialEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialEntry) that is selected by the user.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String
```

Returns the unique id associated with this request. This is for internal use only.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): String
```

Returns the requested credential type.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<BeginGetCredentialOption!>
```
