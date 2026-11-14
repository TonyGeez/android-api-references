Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

# LoadSdkException

Kotlin | [Java](LoadSdkException.md)
| --- | --- |

```
class LoadSdkException : Exception, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.app.sdksandbox.LoadSdkException](LoadSdkException.md) |
| --- | --- | --- | --- |

Exception thrown by loadSdk

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| LoadSdkException Initializes a LoadSdkException with a Throwable and a Bundle. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Bundle](../android.os/Bundle.md) | getExtraInformation Returns the extra error information this exception was constructed with. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLoadSdkErrorCode Returns the result code this exception was constructed with. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [LoadSdkException](LoadSdkException.md)!\> | `https://developer.android.com/reference/kotlin/android/app/sdksandbox/LoadSdkException#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### LoadSdkException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
LoadSdkException(
    cause: Throwable, 
    extraInfo: Bundle)
```

Initializes a LoadSdkException with a Throwable and a Bundle.

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html): The cause of the exception, which is saved for later retrieval by the getCause method. This value cannot be `null`. |
| `extraInfo` | [Bundle](../android.os/Bundle.md): Extra error information. This is empty if there is no such information. This value cannot be `null`. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getExtraInformation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
fun getExtraInformation(): Bundle
```

**Deprecated:** *Deprecated in Java.*

Returns the extra error information this exception was constructed with.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` | The extra error information Bundle. This value cannot be `null`. |

### getLoadSdkErrorCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
fun getLoadSdkErrorCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the result code this exception was constructed with.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The loadSdk result code. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_NOT_FOUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_ALREADY_LOADED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_SDK_DEFINED_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_SDK_SANDBOX_DISABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#LOAD_SDK_INTERNAL_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#SDK_SANDBOX_PROCESS_NOT_AVAILABLE:kotlin.Int` |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    destination: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
| `destination` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<LoadSdkException!>
```

**Deprecated:** *Deprecated in Java.*
