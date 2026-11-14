Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

# CommitBlobResponse

```
class CommitBlobResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.CommitBlobResponse](../android/app/appsearch/CommitBlobResponse.md) |

The response to provide batch operation results of `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchSession#commitBlob(kotlin.collections.MutableSet,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`.

This class is used to retrieve the result of a batch commit operation on a collection of blob handles.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse#CommitBlobResponse(android.app.appsearch.AppSearchBatchResult)(result: https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle!, https://developer.android.com/reference/kotlin/java/lang/Void.html#!>)` Creates a `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse#` with given `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult`. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md)\< [AppSearchBlobHandle](../android/app/appsearch/AppSearchBlobHandle.md)!, [Void](../java/lang/Void.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse#getResult()()` Returns the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult` object containing the results of the commit operation for each `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [CommitBlobResponse](../android/app/appsearch/CommitBlobResponse.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### CommitBlobResponse

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
CommitBlobResponse(result: AppSearchBatchResult<AppSearchBlobHandle!, Void!>)
```

Creates a `https://developer.android.com/reference/kotlin/android/app/appsearch/CommitBlobResponse#` with given `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult`.

| Parameters ||
|---|---|
| `result` | [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md)\< [AppSearchBlobHandle](../android/app/appsearch/AppSearchBlobHandle.md)!, [Void](../java/lang/Void.md)!\>: This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getResult

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun getResult(): AppSearchBatchResult<AppSearchBlobHandle!, Void!>
```

Returns the `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult` object containing the results of the commit operation for each `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle!, https://developer.android.com/reference/kotlin/java/lang/Void.html#!>` | A `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult` maps `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle`s which is a unique identifier for a specific blob being committed to the outcome of that commit. If the operation was successful, the result for that handle is `null`; if there was an error, the result contains an `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchResult` with details of the failure. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<CommitBlobResponse!>
```
