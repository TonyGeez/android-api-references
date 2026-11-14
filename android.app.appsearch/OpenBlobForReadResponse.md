Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

# OpenBlobForReadResponse

```
class OpenBlobForReadResponse : Closeable, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appsearch.OpenBlobForReadResponse](OpenBlobForReadResponse.md) |

The response to provide batch operation results of openBlobForRead.

This class is used to retrieve the result of a batch read operation on a collection of blob handles.

The returned `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` must be closed after use to avoid resource leaks. Failing to close the descriptor will result in system resource exhaustion, as each open `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#` occupies a limited file descriptor in the system.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| OpenBlobForReadResponse Creates a OpenBlobForReadResponse with given AppSearchBatchResult. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | close Closes this stream and releases any system resources associated with it. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [AppSearchBatchResult](AppSearchBatchResult.md)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!, [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!\> | getResult Returns the AppSearchBatchResult object containing the results of the read blob for read operation for each AppSearchBlobHandle. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [OpenBlobForReadResponse](OpenBlobForReadResponse.md)!\> | `https://developer.android.com/reference/kotlin/android/app/appsearch/OpenBlobForReadResponse#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### OpenBlobForReadResponse

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
OpenBlobForReadResponse(result: AppSearchBatchResult<AppSearchBlobHandle!, ParcelFileDescriptor!>)
```

Creates a OpenBlobForReadResponse with given AppSearchBatchResult.

| Parameters ||
|---|---|
| `result` | [AppSearchBatchResult](AppSearchBatchResult.md)\< [AppSearchBlobHandle](AppSearchBlobHandle.md)!, [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)!\>: This value cannot be `null`. |

## Public methods

### close

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes this stream and releases any system resources associated with it. If the stream is already closed then invoking this method has no effect.

As noted in close, cases where the close may fail require careful attention. It is strongly advised to relinquish the underlying resources and to internally *mark* the `Closeable` as closed, prior to throwing the `IOException`.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getResult

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
fun getResult(): AppSearchBatchResult<AppSearchBlobHandle!, ParcelFileDescriptor!>
```

Returns the AppSearchBatchResult object containing the results of the read blob for read operation for each AppSearchBlobHandle.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult<https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBlobHandle!, https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#!>` | A AppSearchBatchResult maps AppSearchBlobHandles which is a unique identifier for a specific blob being committed to the outcome of that read operation. If the operation was successful, the result for that handle is `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#`; if there was an error, the result contains an AppSearchResult with details of the failure. This value cannot be `null`. |

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
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<OpenBlobForReadResponse!>
```
