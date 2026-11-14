# SaveRequest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SaveRequest

Kotlin| [Java](SaveRequest.md) 
| --- | --- |

```
class SaveRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.autofill.SaveRequest](SaveRequest.md) |

This class represents a request to an [autofill provider](AutofillService.md) to save applicable data entered by the user.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SaveRequest.md))`()` <br /> |
| [Bundle](../android.os/Bundle.md)? | [getClientState](SaveRequest.md))`()` Gets the latest client state bundle set by the service in a [fill response](../android/service/autofill/FillResponse.Builder.md)). |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | [getDatasetIds](SaveRequest.md))`()` Gets the ids of the datasets selected by the user, in the order in which they were selected. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FillContext](FillContext.md)!\> | [getFillContexts](SaveRequest.md))`()` Gets the contexts associated with each previous fill request. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SaveRequest.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SaveRequest](SaveRequest.md)!\> | [CREATOR](SaveRequest.md) <br /> |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getClientState

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getClientState(): Bundle?
```

Gets the latest client state bundle set by the service in a [fill response](../android/service/autofill/FillResponse.Builder.md)).

**Note:** Prior to Android [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md), only client state bundles set by [FillResponse.Builder.setClientState(Bundle)](../android/service/autofill/FillResponse.Builder.md))were considered. On Android [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md) and higher, bundles set in the result of an authenticated request through the [android.view.autofill.AutofillManager#EXTRA_CLIENT_STATE](../android.view.autofill/AutofillManager.md) extra are also considered (and take precedence when set).

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------|
| [Bundle](../android.os/Bundle.md)? | The client state. This value may be`null`. |

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

**Note:** Starting on Android [android.os.Build.VERSION_CODES#Q](../android/os/Build.VERSION_CODES.md), it could also include contexts from requests whose [SaveInfo](SaveInfo.md) had the [SaveInfo.FLAG_DELAY_SAVE](SaveInfo.md) flag.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FillContext](FillContext.md)!> | The contexts associated with each previous fill request. This value cannot be`null`. |

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
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SaveRequest!>
```
