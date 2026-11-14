# FeatureInfo

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FeatureInfo

Kotlin| [Java](https://developer.android.com/reference/android/content/pm/FeatureInfo "View this page in Java") 

```
open class FeatureInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.FeatureInfo](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#) |

Definition of a single optional hardware or software feature of an Android device.

This object is used to represent both features supported by a device and features requested by an app. Apps can request that certain features be available as a prerequisite to being installed through the`uses-feature`tag in their manifests.

Starting in [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int), features can have a version, which must always be backwards compatible. That is, a device claiming to support version 3 of a specific feature must support apps requesting version 1 of that feature.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REQUIRED](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#FLAG_REQUIRED:kotlin.Int) Set on [flags](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#flags:kotlin.Int) if this feature has been required by the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_ES_VERSION_UNDEFINED](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#GL_ES_VERSION_UNDEFINED:kotlin.Int) Default value for [reqGlEsVersion](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#reqGlEsVersion:kotlin.Int); |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FeatureInfo](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#FeatureInfo())`()` <br /> |
| [FeatureInfo](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#FeatureInfo(android.content.pm.FeatureInfo))`(`orig:` ` [FeatureInfo](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#describeContents())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getGlEsVersion](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#getGlEsVersion())`()` This method extracts the major and minor version of reqGLEsVersion attribute and returns it as a string. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `parcelableFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [FeatureInfo](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#CREATOR:android.os.Parcelable.Creator) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [flags](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#flags:kotlin.Int) Additional flags. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#name:kotlin.String) The name of this feature, for example "android. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reqGlEsVersion](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#reqGlEsVersion:kotlin.Int) The GLES version used by an application. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [version](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#version:kotlin.Int) If this object represents a feature supported by a device, this is the maximum version of this feature supported by the device. |

## Constants

### FLAG_REQUIRED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_REQUIRED: Int
```

Set on [flags](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#flags:kotlin.Int) if this feature has been required by the application. 

 Value: 1

### GL_ES_VERSION_UNDEFINED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_ES_VERSION_UNDEFINED: Int
```

Default value for [reqGlEsVersion](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#reqGlEsVersion:kotlin.Int); 

 Value: 0

## Public constructors

### FeatureInfo

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FeatureInfo()
```  

### FeatureInfo

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FeatureInfo(orig: FeatureInfo!)
```

## Public methods

### describeContents

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getGlEsVersion

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGlEsVersion(): String!
```

This method extracts the major and minor version of reqGLEsVersion attribute and returns it as a string. Say reqGlEsVersion value of 0x00010002 is returned as 1.2

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String representation of the reqGlEsVersion attribute |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<FeatureInfo!>
```  

### flags

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var flags: Int
```

Additional flags. May be zero or more of [FLAG_REQUIRED](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#FLAG_REQUIRED:kotlin.Int). 

### name

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var name: String!
```

The name of this feature, for example "android.hardware.camera". If this is null, then this is an OpenGL ES version feature as described in [reqGlEsVersion](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#reqGlEsVersion:kotlin.Int). 

### reqGlEsVersion

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var reqGlEsVersion: Int
```

The GLES version used by an application. The upper order 16 bits represent the major version and the lower order 16 bits the minor version. Only valid if [name](https://developer.android.com/reference/kotlin/android/content/pm/FeatureInfo#name:kotlin.String) is null. 

### version

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var version: Int
```

If this object represents a feature supported by a device, this is the maximum version of this feature supported by the device. The device implicitly supports all older versions of this feature.

If this object represents a feature requested by an app, this is the minimum version of the feature required by the app.

When a feature version is undefined by a device, it's assumed to be version 0.
