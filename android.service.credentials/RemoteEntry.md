Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteEntry

Kotlin | [Java](../android/service/credentials/RemoteEntry.md)
| --- | --- |

```
class RemoteEntry : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.RemoteEntry](../android/service/credentials/RemoteEntry.md) |

An entry to be shown on the UI. This entry represents remote execution of a get/create flow whereby credentials are retrieved from, or stored to a remote device.

If user selects this entry, the corresponding `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` set on the `slice` as a androidx.slice.core.SliceAction will get invoked. Once the resulting activity fulfills the required user engagement, the `https://developer.android.com/reference/kotlin/android/app/Activity.html#` result should be set to `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`, and the result of the operation must be set as the activity result. For a get flow, invoked through `https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#onBeginGetCredential(android.service.credentials.BeginGetCredentialRequest,%20android.os.CancellationSignal,%20android.os.OutcomeReceiver)`, providers must set a `https://developer.android.com/reference/kotlin/android/credentials/GetCredentialResponse.html#` on the activity result, against the key `https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#EXTRA_GET_CREDENTIAL_RESPONSE:kotlin.String`. For a creates flow, invoked through `https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#onBeginCreateCredential(android.service.credentials.BeginCreateCredentialRequest,%20android.os.CancellationSignal,%20android.os.OutcomeReceiver)`, providers must set a `https://developer.android.com/reference/kotlin/android/credentials/CreateCredentialResponse.html#` on the activity result against the ket `https://developer.android.com/reference/kotlin/android/service/credentials/CredentialProviderService#EXTRA_CREATE_CREDENTIAL_RESPONSE:kotlin.String`.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry#RemoteEntry(android.app.slice.Slice)(slice: https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#)` Constructs a RemoteEntry to be displayed on the UI. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Slice](../android/app/slice/Slice.md) | `https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry#getSlice()()` Returns the content to be displayed with this remote entry on the UI. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RemoteEntry](../android/service/credentials/RemoteEntry.md)!\> | `https://developer.android.com/reference/kotlin/android/service/credentials/RemoteEntry#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### RemoteEntry

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteEntry(slice: Slice)
```

Constructs a RemoteEntry to be displayed on the UI.

| Parameters ||
|---|---|
| `slice` | [Slice](../android/app/slice/Slice.md): the slice containing the metadata to be shown on the UI, must be constructed through the androidx.credentials.provider Jetpack library; If constructed manually, the `slice` object must contain the non-null properties of the androidx.credentials.provider.RemoteEntry class populated as slice items against specific hints as used in the class's `toSlice` method, since the Android System uses this library to parse the `slice` and extract the required attributes |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getSlice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSlice(): Slice
```

Returns the content to be displayed with this remote entry on the UI.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#` | This value cannot be `null`. |

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
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<RemoteEntry!>
```
