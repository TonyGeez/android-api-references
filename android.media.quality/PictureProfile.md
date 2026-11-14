Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PictureProfile

Kotlin | [Java](PictureProfile.md)
| --- | --- |

```
class PictureProfile : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.quality.PictureProfile](PictureProfile.md) |

Profile for picture quality.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile.Builder` A builder for PictureProfile. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#ERROR_DUPLICATE:kotlin.Int` Error code for creating a profile with existing profile type and name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#ERROR_INVALID_ARGUMENT:kotlin.Int` Error code for invalid argument. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#ERROR_NOT_ALLOWLISTED:kotlin.Int` Error code for the case when an operation requires an allowlist but the caller is not in the list. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#ERROR_NO_PERMISSION:kotlin.Int` Error code for missing necessary permission to handle the profiles. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#ERROR_UNKNOWN:kotlin.Int` Error code for unknown errors. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#TYPE_APPLICATION:kotlin.Int` Application profile type. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#TYPE_SYSTEM:kotlin.Int` System profile type. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getInputId Gets the input ID if the profile is for a TV input. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getName Gets the profile name. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getPackageName Gets the package name of this profile. |
| [PersistableBundle](../android.os/PersistableBundle.md) | getParameters Gets the parameters of this profile. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getProfileId Gets profile ID. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getProfileType Gets profile type. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PictureProfile](PictureProfile.md)!\> | `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ERROR_DUPLICATE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_DUPLICATE: Int
```

Error code for creating a profile with existing profile type and name.

 Value: 2

**See Also**

- getProfileType
- getName

### ERROR_INVALID_ARGUMENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_INVALID_ARGUMENT: Int
```

Error code for invalid argument.

 Value: 3

### ERROR_NOT_ALLOWLISTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NOT_ALLOWLISTED: Int
```

Error code for the case when an operation requires an allowlist but the caller is not in the list.

 Value: 4

**See Also**

### ERROR_NO_PERMISSION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NO_PERMISSION: Int
```

Error code for missing necessary permission to handle the profiles.

 Value: 1

### ERROR_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNKNOWN: Int
```

Error code for unknown errors.

 Value: 0

### TYPE_APPLICATION

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_APPLICATION: Int
```

Application profile type.

A profile of application type is managed by the package returned by getPackageName.

 Value: 2

### TYPE_SYSTEM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SYSTEM: Int
```

System profile type.

A profile of system type is managed by the system, and readable to the package returned by getPackageName.

 Value: 1

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getInputId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInputId(): String?
```

Gets the input ID if the profile is for a TV input.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the corresponding TV input ID; `null` if the profile is not associated with a TV input. |

**See Also**

- getId

### getName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

Gets the profile name.

### getPackageName

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String?
```

Gets the package name of this profile.

The package name defines the user of a profile. Only this specific package and system app can access to this profile.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the package name; `null` if the profile is built locally using `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile.Builder` and the package is not set. |

### getParameters

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParameters(): PersistableBundle
```

Gets the parameters of this profile.

The keys of commonly used parameters can be found in `https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityContract.PictureQuality`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#` | The profile parameters. Empty bundle if parameters are not included in a query. |

### getProfileId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProfileId(): String?
```

Gets profile ID.

A profile ID is a globally unique ID generated and assigned by the system. For profile objects retrieved from system (e.g getAvailablePictureProfiles) this profile ID is non-null; For profiles built locally with `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile.Builder`, it's `null`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the unique profile ID; `null` if the profile is built locally with `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile.Builder`. |

### getProfileType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProfileType(): Int
```

Gets profile type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#TYPE_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#TYPE_APPLICATION:kotlin.Int` |

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
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<PictureProfile!>
```
