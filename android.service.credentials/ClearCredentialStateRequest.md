# ClearCredentialStateRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClearCredentialStateRequest

Kotlin| [Java](https://developer.android.com/reference/android/service/credentials/ClearCredentialStateRequest "View this page in Java") 
| --- | --- |

```
class ClearCredentialStateRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.ClearCredentialStateRequest](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#) |

A request class for clearing a user's credential state. Providers must clear the credential state when they receive this request.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClearCredentialStateRequest](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#ClearCredentialStateRequest(android.service.credentials.CallingAppInfo,%20android.os.Bundle))`(`callingAppInfo:` ` [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo)`, `data:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Constructs a [ClearCredentialStateRequest](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#). |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#describeContents())`()` <br /> |
| [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo) | [getCallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#getCallingAppInfo())`()` Returns the calling app info containing information pertaining to the calling app. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getData](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#getData())`()` Returns the request data. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ClearCredentialStateRequest](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### ClearCredentialStateRequest

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClearCredentialStateRequest(
    callingAppInfo: CallingAppInfo, 
    data: Bundle)
```

Constructs a [ClearCredentialStateRequest](https://developer.android.com/reference/kotlin/android/service/credentials/ClearCredentialStateRequest#).

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):the request data This value cannot be`null`. |
| `callingAppInfo` | [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo):This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCallingAppInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallingAppInfo(): CallingAppInfo
```

Returns the calling app info containing information pertaining to the calling app.

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------|
| [CallingAppInfo](https://developer.android.com/reference/kotlin/android/service/credentials/CallingAppInfo) | This value cannot be`null`. |

### getData

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): Bundle
```

Returns the request data.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<ClearCredentialStateRequest!>
```
