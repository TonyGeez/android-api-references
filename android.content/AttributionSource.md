Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AttributionSource

Kotlin | [Java](https://developer.android.com/reference/android/content/AttributionSource "View this page in Java")

```
class AttributionSource : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource#) |

This class represents a source to which access to permission protected data should be attributed. Attribution sources can be chained to represent cases where the protected data would flow through several applications. For example, app A may ask app B for contacts and in turn app B may ask app C for contacts. In this case, the attribution chain would be A -\> B -\> C and the data flow would be C -\> B -\> A. There are two main benefits of using the attribution source mechanism: avoid doing explicit permission checks on behalf of the calling app if you are accessing private data on their behalf to send back; avoid double data access blaming which happens as you check the calling app's permissions and when you access the data behind these permissions (for runtime permissions). Also if not explicitly blaming the caller the data access would be counted towards your app vs to the previous app where yours was just a proxy.

Every `https://developer.android.com/reference/kotlin/android/content/Context` has an attribution source and you can get it via `https://developer.android.com/reference/kotlin/android/content/Context#getAttributionSource()` representing itself, which is a chain of one. You can attribute work to another app, or more precisely to a chain of apps, through which the data you would be accessing would flow, via `https://developer.android.com/reference/kotlin/android/content/Context#createContext(android.content.ContextParams)` plus specifying an attribution source for the next app to receive the protected data you are accessing via `https://developer.android.com/reference/kotlin/android/content/AttributionSource.Builder#setNext(android.content.AttributionSource)`. Creating this attribution chain ensures that the datasource would check whether every app in the attribution chain has permission to access the data before releasing it. The datasource will also record appropriately that this data was accessed by the apps in the sequence if the data is behind a sensitive permission (e.g. dangerous). Again, this is useful if you are accessing the data on behalf of another app, for example a speech recognizer using the mic so it can provide recognition to a calling app.

You can create an attribution chain of you and any other app without any verification as this is something already available via the `https://developer.android.com/reference/kotlin/android/app/AppOpsManager.html#` APIs. This is supported to handle cases where you don't have access to the caller's attribution source and you can directly use the `https://developer.android.com/reference/kotlin/android/content/AttributionSource.Builder` APIs. However, if the data flows through more than two apps (more than you access the data for the caller) you need to have a handle to the `https://developer.android.com/reference/kotlin/android/content/AttributionSource#` for the calling app's context in order to create an attribution context. This means you either need to have an API for the other app to send you its attribution source or use a platform API that pipes the callers attribution source.

You cannot forge an attribution chain without the participation of every app in the attribution chain (aside of the special case mentioned above). To create an attribution source that is trusted you need to create an attribution context that points to an attribution source that was explicitly created by the app that it refers to, recursively.

Since creating an attribution context leads to all permissions for apps in the attribution chain being checked, you need to expect getting a security exception when accessing permission protected APIs since some app in the chain may not have the permission.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/content/AttributionSource.Builder` A builder for `https://developer.android.com/reference/kotlin/android/content/AttributionSource#` |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#checkCallingUid()()` If you are handling an IPC and you don't trust the caller you need to validate whether the attribution source is one for the calling app to prevent the caller to pass you a source from another app without including themselves in the attribution chain. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#enforceCallingUid()()` If you are handling an IPC and you don't trust the caller you need to validate whether the attribution source is one for the calling app to prevent the caller to pass you a source from another app without including themselves in the attribution chain. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#getAttributionTag()()` The attribution tag of the app accessing the permission protected data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#getDeviceId()()` Gets the device ID for this attribution source. |
| [AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource#)? | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#getNext()()` The next app to receive the permission protected data. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#getPackageName()()` The package that is accessing the permission protected data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#getPid()()` The PID that is accessing the permission protected data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#getUid()()` The UID that is accessing the permission protected data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#isTrusted(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context)` Checks whether this attribution source can be trusted. |
| static [AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource#) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#myAttributionSource()()` Returns a generic `https://developer.android.com/reference/kotlin/android/content/AttributionSource#` that represents the entire calling process. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AttributionSource](https://developer.android.com/reference/kotlin/android/content/AttributionSource#)!\> | `https://developer.android.com/reference/kotlin/android/content/AttributionSource#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public methods

### checkCallingUid

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun checkCallingUid(): Boolean
```

If you are handling an IPC and you don't trust the caller you need to validate whether the attribution source is one for the calling app to prevent the caller to pass you a source from another app without including themselves in the attribution chain.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | if the attribution source cannot be trusted to be from the caller. |

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### enforceCallingUid

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enforceCallingUid(): Unit
```

If you are handling an IPC and you don't trust the caller you need to validate whether the attribution source is one for the calling app to prevent the caller to pass you a source from another app without including themselves in the attribution chain.

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the attribution source cannot be trusted to be from the caller. |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAttributionTag

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAttributionTag(): String?
```

The attribution tag of the app accessing the permission protected data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getDeviceId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeviceId(): Int
```

Gets the device ID for this attribution source. Attribution source can set the device ID using `https://developer.android.com/reference/kotlin/android/content/AttributionSource.Builder#setDeviceId(kotlin.Int)`, the default device ID is `https://developer.android.com/reference/kotlin/android/content/Context#DEVICE_ID_DEFAULT:kotlin.Int`.

This device ID is used for permissions checking during attribution source validation.

### getNext

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNext(): AttributionSource?
```

The next app to receive the permission protected data.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/AttributionSource#?` | This value may be `null`. |

### getPackageName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPackageName(): String?
```

The package that is accessing the permission protected data.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getPid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPid(): Int
```

The PID that is accessing the permission protected data.

### getUid

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUid(): Int
```

The UID that is accessing the permission protected data.

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isTrusted

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isTrusted(context: Context): Boolean
```

Checks whether this attribution source can be trusted. That is whether the app it refers to created it and provided to the attribution chain.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context): Context handle. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this is a trusted source. |

### myAttributionSource

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun myAttributionSource(): AttributionSource
```

Returns a generic `https://developer.android.com/reference/kotlin/android/content/AttributionSource#` that represents the entire calling process.

Callers are *strongly* encouraged to use a more specific attribution source whenever possible, such as from `https://developer.android.com/reference/kotlin/android/content/Context#getAttributionSource()`, since that enables developers to have more detailed and scoped control over attribution within sub-components of their app.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/AttributionSource#` | a generic `https://developer.android.com/reference/kotlin/android/content/AttributionSource#` representing the entire calling process. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | when no accurate `https://developer.android.com/reference/kotlin/android/content/AttributionSource#` can be determined |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/Context#createAttributionContext(kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/content/Context#getAttributionTag()`

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AttributionSource!>
```
