Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppFunctionUriGrant

```
class AppFunctionUriGrant : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.appfunctions.AppFunctionUriGrant](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#) |

`https://developer.android.com/reference/kotlin/android/net/Uri.html#` for which access permission is to be granted to the caller of android.app.appfunctions.AppFunctionManager#executeAppFunction, provided to `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse`.

This class encapsulates a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` along with the specific access mode flags (e.g., `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int`) that define the type of access to be granted for that URI.

When an AppFunction implementation returns an `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse` containing a `https://developer.android.com/reference/kotlin/android/net/Uri.html#`, the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` itself must be placed in either `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getResultDocument()` or `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getExtras()`. Concurrently, a corresponding `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#` detailing the intended permissions must be added to `https://developer.android.com/reference/kotlin/android/app/appfunctions/ExecuteAppFunctionResponse#getUriGrants()`. This ensures the caller receives the necessary access rights to the returned `https://developer.android.com/reference/kotlin/android/net/Uri.html#`.

To succeed, the content provider owning the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` must have set the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestProvider_grantUriPermissions:kotlin.Int` attribute in its manifest or included in the `https://developer.android.com/reference/kotlin/android/R.styleable.html#AndroidManifestGrantUriPermission:kotlin.IntArray` tag.

These grants typically persist until the device reboots unles `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int` is set and the receiver calls `https://developer.android.com/reference/kotlin/android/content/ContentResolver.html#takePersistableUriPermission(android.net.Uri,%20kotlin.Int)`. The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` owner may consider clearing data associated with these URIs after a reboot.

## Summary

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#AppFunctionUriGrant(android.net.Uri,%20kotlin.Int)(uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, modeFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#` |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#getModeFlags()()` Returns the access mode flags. |
| --- | --- |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#getUri()()` Returns the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to be granted. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AppFunctionUriGrant](https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#)!\> | `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### AppFunctionUriGrant

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AppFunctionUriGrant(
    uri: Uri, 
    modeFlags: Int)
```

Constructs an `https://developer.android.com/reference/kotlin/android/app/appfunctions/AppFunctionUriGrant#`

| Parameters ||
|---|---|
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to be granted. This value cannot be `null`. |
| `modeFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The access mode flags. This value must include at least one of `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int`. It may optionally also include `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PREFIX_URI_PERMISSION:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PREFIX_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int` |

## Public methods

### describeContents

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getModeFlags

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getModeFlags(): Int
```

Returns the access mode flags.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_READ_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_WRITE_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PREFIX_URI_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_GRANT_PERSISTABLE_URI_PERMISSION:kotlin.Int` |

### getUri

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUri(): Uri
```

Returns the `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to be granted.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#` | This value cannot be `null`. |

### hashCode

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AppFunctionUriGrant!>
```
