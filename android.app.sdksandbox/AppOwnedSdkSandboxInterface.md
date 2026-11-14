# AppOwnedSdkSandboxInterface

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions)

# AppOwnedSdkSandboxInterface

Kotlin| [Java](https://developer.android.com/reference/android/app/sdksandbox/AppOwnedSdkSandboxInterface "View this page in Java") 

```
class AppOwnedSdkSandboxInterface : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.sdksandbox.AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#) |

Represents a channel for an SDK in the sandbox process to interact with the app.

The SDK and the app can agree on a binder interface to be implemented by the app and shared via an object of [AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#).

The app registers the AppOwnedSdkSandboxInterfaces using [android.app.sdksandbox.SdkSandboxManager#registerAppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#registerAppOwnedSdkSandboxInterface(android.app.sdksandbox.AppOwnedSdkSandboxInterface)).

The SDK in sandbox process can then query the list of registered AppOwnedSdkSandboxInterfaces using [android.app.sdksandbox.sdkprovider.SdkSandboxController#getAppOwnedSdkSandboxInterfaces](https://developer.android.com/reference/kotlin/android/app/sdksandbox/sdkprovider/SdkSandboxController#getAppOwnedSdkSandboxInterfaces()).

Once SDK has the AppOwnedSdkSandboxInterface it wants to communicate with, it will have to cast the binder object from [getInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#getInterface())to the prearranged interface before initiating the communication.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#AppOwnedSdkSandboxInterface(kotlin.String,%20kotlin.Long,%20android.os.IBinder))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `version:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `binder:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#describeContents())`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#) | [getInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#getInterface())`()` Returns binder object associated with AppOwnedSdkSandboxInterface. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#getName())`()` Returns the name used to register the AppOwnedSdkSandboxInterface. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#getVersion())`()` Returns the version used to register the AppOwnedSdkSandboxInterface. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### AppOwnedSdkSandboxInterface

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
AppOwnedSdkSandboxInterface(
    name: String, 
    version: Long, 
    binder: IBinder)
```

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `binder` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#):This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getInterface

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
fun getInterface(): IBinder
```

Returns binder object associated with AppOwnedSdkSandboxInterface.

The SDK and the app can agree on a binder interface to be implemented by the app and shared via this object, see [AppOwnedSdkSandboxInterface](https://developer.android.com/reference/kotlin/android/app/sdksandbox/AppOwnedSdkSandboxInterface#).

The SDK in the sandbox will have to cast the binder object received from this method to the agreed upon interface before using it.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#) | This value cannot be`null`. |

### getName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
fun getName(): String
```

Returns the name used to register the AppOwnedSdkSandboxInterface.

App can register only one interface of given name.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getVersion

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
fun getVersion(): Long
```

Returns the version used to register the AppOwnedSdkSandboxInterface.

A version may be chosen by an app, and used to communicate any updates the app makes to this implementation. 

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<AppOwnedSdkSandboxInterface!>
```
