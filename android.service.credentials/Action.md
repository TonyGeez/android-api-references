Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Action

Kotlin | [Java](../android/service/credentials/Action.md)
| --- | --- |

```
class Action : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.credentials.Action](../android/service/credentials/Action.md) |

An action defined by the provider that intents into the provider's app for specific user actions.

If user selects this action entry, the corresponding `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` set on the `slice` as a androidx.slice.core.SliceAction will get invoked.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/service/credentials/Action#Action(android.app.slice.Slice)(slice: https://developer.android.com/reference/kotlin/android/app/slice/Slice.html#)` Constructs an action to be displayed on the UI. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/Action#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Slice](../android/app/slice/Slice.md) | `https://developer.android.com/reference/kotlin/android/service/credentials/Action#getSlice()()` Returns a `Slice` object containing the display content to be displayed on the UI. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/service/credentials/Action#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [Action](../android/service/credentials/Action.md)!\> | `https://developer.android.com/reference/kotlin/android/service/credentials/Action#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### Action

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Action(slice: Slice)
```

Constructs an action to be displayed on the UI.

Actions must be used for any provider related operations, such as opening the provider app, intenting straight into certain app activities like 'manage credentials', top level authentication before displaying any content etc.

See details on usage of `Action` for various actionable entries in `https://developer.android.com/reference/kotlin/android/service/credentials/BeginCreateCredentialResponse` and `https://developer.android.com/reference/kotlin/android/service/credentials/BeginGetCredentialResponse`.

| Parameters ||
|---|---|
| `slice` | [Slice](../android/app/slice/Slice.md): the slice containing the metadata to be shown on the UI, must be constructed through the androidx.credentials.provider Jetpack library; If constructed manually, the `slice` object must contain the non-null properties of the androidx.credentials.provider.Action class populated as slice items against specific hints as used in the class's `toSlice` method, since the Android System uses this library to parse the `slice` and extract the required attributes |

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

Returns a `Slice` object containing the display content to be displayed on the UI.

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
static val CREATOR: Parcelable.Creator<Action!>
```
