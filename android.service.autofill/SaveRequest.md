# SaveRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SaveRequest

Kotlin| [Java](https://developer.android.com/reference/android/service/autofill/SaveRequest "View this page in Java") 
| --- | --- |

```
class SaveRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.SaveRequest](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest#) |

This class represents a request to an [autofill provider](https://developer.android.com/reference/kotlin/android/service/autofill/AutofillService) to save applicable data entered by the user.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest#describeContents())`()` <br /> |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getClientState](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest#getClientState())`()` Gets the latest client state bundle set by the service in a [fill response](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setClientState(android.os.Bundle)). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getDatasetIds](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest#getDatasetIds())`()` Gets the ids of the datasets selected by the user, in the order in which they were selected. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FillContext](https://developer.android.com/reference/kotlin/android/service/autofill/FillContext)!\> | [getFillContexts](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest#getFillContexts())`()` Gets the contexts associated with each previous fill request. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SaveRequest](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/autofill/SaveRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getClientState

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientState(): Bundle?
```

Gets the latest client state bundle set by the service in a [fill response](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setClientState(android.os.Bundle)).

**Note:** Prior to Android [android.os.Build.VERSION_CODES#P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int), only client state bundles set by [FillResponse.Builder.setClientState(Bundle)](https://developer.android.com/reference/kotlin/android/service/autofill/FillResponse.Builder#setClientState(android.os.Bundle))were considered. On Android [android.os.Build.VERSION_CODES#P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int) and higher, bundles set in the result of an authenticated request through the [android.view.autofill.AutofillManager#EXTRA_CLIENT_STATE](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillManager.html#EXTRA_CLIENT_STATE:kotlin.String) extra are also considered (and take precedence when set).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | The client state. This value may be`null`. |

### getDatasetIds

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDatasetIds(): MutableList<String!>?
```

Gets the ids of the datasets selected by the user, in the order in which they were selected.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>? | This value may be`null`. |

### getFillContexts

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFillContexts(): MutableList<FillContext!>
```

Gets the contexts associated with each previous fill request.

**Note:** Starting on Android [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int), it could also include contexts from requests whose [SaveInfo](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo) had the [SaveInfo.FLAG_DELAY_SAVE](https://developer.android.com/reference/kotlin/android/service/autofill/SaveInfo#FLAG_DELAY_SAVE:kotlin.Int) flag.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FillContext](https://developer.android.com/reference/kotlin/android/service/autofill/FillContext)!> | The contexts associated with each previous fill request. This value cannot be`null`. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SaveRequest!>
```
