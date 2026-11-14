Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SandboxedSdk

```
class SandboxedSdk : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.sdksandbox.SandboxedSdk](../android/app/sdksandbox/SandboxedSdk.md) |

> [!CAUTION]
> **This class was deprecated in API level 37.**
>
> The SDK sandbox is no longer supported.

Represents an SDK loaded in the sandbox process.

Returned in response to `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`, on success. An application can obtain it by calling `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. It should use this object to obtain an interface to the SDK through `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#getInterface()`.

The SDK should create it when `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdkProvider#onLoadSdk(android.os.Bundle)` is called, and drop all references to it when `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdkProvider#beforeUnloadSdk()` is called. Additionally, the SDK should fail calls made to the `IBinder` returned from `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#getInterface()` after `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdkProvider#beforeUnloadSdk()` has been called.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#SandboxedSdk(android.os.IBinder)(sdkInterface: https://developer.android.com/reference/kotlin/android/os/IBinder.html#)` Creates a `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#` object. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [IBinder](../android/os/IBinder.md)? | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#getInterface()()` Returns the interface to the SDK that was loaded in response to `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| [SharedLibraryInfo](../android/content/pm/SharedLibraryInfo.md) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#getSharedLibraryInfo()()` Returns the `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#` for the SDK. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SandboxedSdk](../android/app/sdksandbox/SandboxedSdk.md)!\> | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### SandboxedSdk

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
SandboxedSdk(sdkInterface: IBinder)
```

Creates a `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#` object.

| Parameters ||
|---|---|
| `sdkInterface` | [IBinder](../android/os/IBinder.md): The SDK's interface. This will be the entrypoint into the sandboxed SDK for the application. The SDK should keep this valid until it's loaded in the sandbox, and start failing calls to this interface once it has been unloaded. This interface can later be retrieved using `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#getInterface()`. This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getInterface

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInterface(): IBinder?
```

**Deprecated:** *Deprecated in Java.*

Returns the interface to the SDK that was loaded in response to `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#loadSdk(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. A `null` interface is returned if the Binder has since become unavailable, in response to the SDK being unloaded.

### getSharedLibraryInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 5](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSharedLibraryInfo(): SharedLibraryInfo
```

**Deprecated:** *Deprecated in Java.*

Returns the `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#` for the SDK.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the system service has not yet attached `https://developer.android.com/reference/kotlin/android/content/pm/SharedLibraryInfo.html#` to the `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SandboxedSdk#` object sent by the SDK. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SandboxedSdk!>
```

**Deprecated:** *Deprecated in Java.*
