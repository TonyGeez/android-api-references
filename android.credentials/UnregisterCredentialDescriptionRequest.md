# UnregisterCredentialDescriptionRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnregisterCredentialDescriptionRequest

Kotlin| [Java](https://developer.android.com/reference/android/credentials/UnregisterCredentialDescriptionRequest "View this page in Java") 
| --- | --- |

```
class UnregisterCredentialDescriptionRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.credentials.UnregisterCredentialDescriptionRequest](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest#) |

A request to unregister a [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) that contains an actively provisioned [Credential](https://developer.android.com/reference/kotlin/android/credentials/Credential) represented by a [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription). \*

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnregisterCredentialDescriptionRequest](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest#UnregisterCredentialDescriptionRequest(android.credentials.CredentialDescription))`(`credentialDescription:` ` [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription)`)` <br /> |
| [UnregisterCredentialDescriptionRequest](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest#UnregisterCredentialDescriptionRequest(kotlin.collections.MutableSet))`(`credentialDescriptions:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription)!>`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest#describeContents())`()` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription)!\> | [getCredentialDescriptions](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest#getCredentialDescriptions())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [UnregisterCredentialDescriptionRequest](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/credentials/UnregisterCredentialDescriptionRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### UnregisterCredentialDescriptionRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnregisterCredentialDescriptionRequest(credentialDescription: CredentialDescription)
```

| Parameters ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `credentialDescription` | [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription):This value cannot be`null`. |

### UnregisterCredentialDescriptionRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnregisterCredentialDescriptionRequest(credentialDescriptions: MutableSet<CredentialDescription!>)
```

| Parameters ||
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `credentialDescriptions` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription)!\>:This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCredentialDescriptions

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCredentialDescriptions(): MutableSet<CredentialDescription!>
```

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [CredentialDescription](https://developer.android.com/reference/kotlin/android/credentials/CredentialDescription)!> | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<UnregisterCredentialDescriptionRequest!>
```
