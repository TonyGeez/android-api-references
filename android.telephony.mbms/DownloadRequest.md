# DownloadRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DownloadRequest

Kotlin| [Java](https://developer.android.com/reference/android/telephony/mbms/DownloadRequest "View this page in Java") 
| --- | --- |

```
class DownloadRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#) |

Describes a request to download files over cell-broadcast. Instances of this class should be created by the app when requesting a download, and instances of this class will be passed back to the app when the middleware updates the status of the download.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest.Builder) <br /> |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getDestinationUri](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#getDestinationUri())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFileServiceId](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#getFileServiceId())`()` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxAppIntentSize](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#getMaxAppIntentSize())`()` Maximum permissible length for the app's destination path, when serialized via [Uri.toString()](https://developer.android.com/reference/kotlin/android/net/Uri.html#toString()). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxDestinationUriSize](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#getMaxDestinationUriSize())`()` Maximum permissible length for the app's download-completion intent, when serialized via [Intent.toUri(int)](https://developer.android.com/reference/kotlin/android/content/Intent.html#toUri(kotlin.Int)). |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [getSourceUri](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#getSourceUri())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSubscriptionId](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#getSubscriptionId())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#hashCode())`()` <br /> |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [toByteArray](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#toByteArray())`()` This method returns a byte array that may be persisted to disk and restored to a [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDestinationUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDestinationUri(): Uri!
```

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | The destination [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) of the downloaded file. |

### getFileServiceId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFileServiceId(): String!
```

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The ID of the file service to download from. |

### getMaxAppIntentSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMaxAppIntentSize(): Int
```

Maximum permissible length for the app's destination path, when serialized via [Uri.toString()](https://developer.android.com/reference/kotlin/android/net/Uri.html#toString()). 

### getMaxDestinationUriSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMaxDestinationUriSize(): Int
```

Maximum permissible length for the app's download-completion intent, when serialized via [Intent.toUri(int)](https://developer.android.com/reference/kotlin/android/content/Intent.html#toUri(kotlin.Int)). 

### getSourceUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSourceUri(): Uri!
```

| Return ||
|------------------------------------------------------------------------------|---------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | The source URI to download from |

### getSubscriptionId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSubscriptionId(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The subscription ID on which to perform MBMS operations. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toByteArray

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toByteArray(): ByteArray!
```

This method returns a byte array that may be persisted to disk and restored to a [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#). The instance of [DownloadRequest](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest#) persisted by this method may be recovered via[Builder.fromSerializedRequest(byte[])](https://developer.android.com/reference/kotlin/android/telephony/mbms/DownloadRequest.Builder#fromSerializedRequest(kotlin.ByteArray)).

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | A byte array of data to persist. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<DownloadRequest!>
```
