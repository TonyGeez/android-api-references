# AppOwnedSdkSandboxInterface

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions)

# AppOwnedSdkSandboxInterface

Kotlin| [Java](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md) 
| --- | --- |

```
class AppOwnedSdkSandboxInterface : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.sdksandbox.AppOwnedSdkSandboxInterface](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md) |

Represents a channel for an SDK in the sandbox process to interact with the app.

The SDK and the app can agree on a binder interface to be implemented by the app and shared via an object of [AppOwnedSdkSandboxInterface](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md).

The app registers the AppOwnedSdkSandboxInterfaces using [android.app.sdksandbox.SdkSandboxManager#registerAppOwnedSdkSandboxInterface](../android/app/sdksandbox/SdkSandboxManager.md)).

The SDK in sandbox process can then query the list of registered AppOwnedSdkSandboxInterfaces using [android.app.sdksandbox.sdkprovider.SdkSandboxController#getAppOwnedSdkSandboxInterfaces](../android/app/sdksandbox/sdkprovider/SdkSandboxController.md)).

Once SDK has the AppOwnedSdkSandboxInterface it wants to communicate with, it will have to cast the binder object from [getInterface](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md))to the prearranged interface before initiating the communication.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AppOwnedSdkSandboxInterface](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `version:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `binder:` ` [IBinder](../android/os/IBinder.md)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md))`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [IBinder](../android/os/IBinder.md) | [getInterface](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md))`()` Returns binder object associated with AppOwnedSdkSandboxInterface. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md))`()` Returns the name used to register the AppOwnedSdkSandboxInterface. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getVersion](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md))`()` Returns the version used to register the AppOwnedSdkSandboxInterface. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AppOwnedSdkSandboxInterface](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md)!\> | [CREATOR](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md) <br /> |

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
| `binder` | [IBinder](../android/os/IBinder.md):This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/os/Parcelable.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getInterface

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
fun getInterface(): IBinder
```

Returns binder object associated with AppOwnedSdkSandboxInterface.

The SDK and the app can agree on a binder interface to be implemented by the app and shared via this object, see [AppOwnedSdkSandboxInterface](../android/app/sdksandbox/AppOwnedSdkSandboxInterface.md).

The SDK in the sandbox will have to cast the binder object received from this method to the agreed upon interface before using it.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [IBinder](../android/os/IBinder.md) | This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 8](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<AppOwnedSdkSandboxInterface!>
```
