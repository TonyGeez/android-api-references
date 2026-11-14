# CreateEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CreateEntry

Kotlin| [Java](https://developer.android.com/reference/android/service/credentials/CreateEntry "View this page in Java") 

```
class CreateEntry : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.credentials.CreateEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CreateEntry#) |

An entry to be shown on the UI. This entry represents where the credential to be created will be stored. Examples include user's account, family group etc.

If user selects this entry, the corresponding [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) set on the`slice`as a androidx.slice.core.SliceAction will get invoked. Once the resulting activity fulfills the required user engagement, the [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) result should be set to [android.app.Activity#RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int), and the [CredentialProviderService.EXTRA_CREATE_CREDENTIAL_RESPONSE](https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#EXTRA_CREATE_CREDENTIAL_RESPONSE:kotlin.String) must be set with a [android.credentials.CreateCredentialResponse](https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialResponse.html#) object.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CreateEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CreateEntry#CreateEntry(android.app.slice.Slice))`(`slice:` ` [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#)`)` Constructs a CreateEntry to be displayed on the UI. |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/credentials/CreateEntry#describeContents())`()` <br /> |
| [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) | [getSlice](https://developer.android.com/reference/kotlin/android/service/credentials/CreateEntry#getSlice())`()` Returns the content to be displayed with this create entry on the UI. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/credentials/CreateEntry#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CreateEntry](https://developer.android.com/reference/kotlin/android/service/credentials/CreateEntry#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/credentials/CreateEntry#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### CreateEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CreateEntry(slice: Slice)
```

Constructs a CreateEntry to be displayed on the UI.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `slice` | [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#):the slice containing the metadata to be shown on the UI, must be constructed through the androidx.credentials.provider Jetpack library; If constructed manually, the`slice`object must contain the non-null properties of the androidx.credentials.provider.CreateEntry class populated as slice items against specific hints as used in the class's`toSlice`method, since the Android System uses this library to parse the`slice`and extract the required attributes |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getSlice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSlice(): Slice
```

Returns the content to be displayed with this create entry on the UI.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#) | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<CreateEntry!>
```
