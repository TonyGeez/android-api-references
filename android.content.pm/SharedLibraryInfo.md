Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SharedLibraryInfo

Kotlin | [Java](SharedLibraryInfo.md)
| --- | --- |

```
class SharedLibraryInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.SharedLibraryInfo](SharedLibraryInfo.md) |

This class provides information for a shared library. There are four types of shared libraries: builtin - non-updatable part of the OS; dynamic - updatable backwards-compatible dynamically linked; static - non backwards-compatible emulating static linking; SDK - updatable backwards-incompatible dynamically loaded.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_BUILTIN:kotlin.Int` Shared library type: this library is a part of the OS and cannot be updated or uninstalled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_DYNAMIC:kotlin.Int` Shared library type: this library is backwards-compatible, can be updated, and updates can be uninstalled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_SDK_PACKAGE:kotlin.Int` SDK package shared library type: this library is **not** compatible between versions, can be updated and updates can be uninstalled. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_STATIC:kotlin.Int` Shared library type: this library is **not** backwards -compatible, can be updated and updates can be uninstalled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#VERSION_UNDEFINED:kotlin.Int` Constant for referring to an undefined version. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#getCertDigests()()` Gets the list of certificate digests for the shared library. |
| [VersionedPackage](VersionedPackage.md) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#getDeclaringPackage()()` Gets the package that declares the library. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [VersionedPackage](VersionedPackage.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#getDependentPackages()()` Gets the packages that depend on the library. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#getLongVersion()()` Gets the version of the library. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#getName()()` Gets the library name an app defines in its manifest to depend on the library. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#getType()()` Gets the type of this library. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#getVersion()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(parcel: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SharedLibraryInfo](SharedLibraryInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### TYPE_BUILTIN

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BUILTIN: Int
```

Shared library type: this library is a part of the OS and cannot be updated or uninstalled.

 Value: 0

### TYPE_DYNAMIC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_DYNAMIC: Int
```

Shared library type: this library is backwards-compatible, can be updated, and updates can be uninstalled. Clients link against the latest version of the library.

 Value: 1

### TYPE_SDK_PACKAGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_SDK_PACKAGE: Int
```

SDK package shared library type: this library is **not** compatible between versions, can be updated and updates can be uninstalled. Clients depend on a specific version of the library. SDK packages are not loaded automatically by the OS and rely e.g. on 3P libraries to make them available for the clients.

 Value: 3

### TYPE_STATIC

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_STATIC: Int
```

Shared library type: this library is **not** backwards -compatible, can be updated and updates can be uninstalled. Clients link against a specific version of the library. Static shared libraries simulate static linking while allowing for multiple clients to reuse the same instance of the library.

 Value: 2

### VERSION_UNDEFINED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VERSION_UNDEFINED: Int
```

Constant for referring to an undefined version.

 Value: -1

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getCertDigests

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCertDigests(): MutableList<String!>
```

Gets the list of certificate digests for the shared library.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The list of certificate digests. This value cannot be `null`. |

### getDeclaringPackage

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeclaringPackage(): VersionedPackage
```

Gets the package that declares the library.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage` | The package declaring the library. This value cannot be `null`. |

### getDependentPackages

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDependentPackages(): MutableList<VersionedPackage!>
```

Gets the packages that depend on the library. NOTE: the list also contains the result of #getOptionalDependentPackages.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/content/pm/VersionedPackage!>` | The dependent packages. This value cannot be `null`. |

### getLongVersion

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLongVersion(): Long
```

Gets the version of the library. For `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_STATIC:kotlin.Int` libraries this is the declared version and for `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_DYNAMIC:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_BUILTIN:kotlin.Int` it is `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#VERSION_UNDEFINED:kotlin.Int` as these are not versioned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The version. Value is -1 or greater |

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String!
```

Gets the library name an app defines in its manifest to depend on the library.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The name. |

### getType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Gets the type of this library.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The library type. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_BUILTIN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_DYNAMIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_STATIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#TYPE_SDK_PACKAGE:kotlin.Int` |

### getVersion

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVersion(): Int
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo#getLongVersion()` instead.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is -1 or greater |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SharedLibraryInfo!>
```
