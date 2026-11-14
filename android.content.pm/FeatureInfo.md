# FeatureInfo

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FeatureInfo

Kotlin| [Java](FeatureInfo.md) 
| --- | --- |

```
open class FeatureInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.FeatureInfo](FeatureInfo.md) |

Definition of a single optional hardware or software feature of an Android device.

This object is used to represent both features supported by a device and features requested by an app. Apps can request that certain features be available as a prerequisite to being installed through the`uses-feature`tag in their manifests.

Starting in [android.os.Build.VERSION_CODES#N](../android/os/Build.VERSION_CODES.md), features can have a version, which must always be backwards compatible. That is, a device claiming to support version 3 of a specific feature must support apps requesting version 1 of that feature.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_REQUIRED](FeatureInfo.md) Set on [flags](FeatureInfo.md) if this feature has been required by the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GL_ES_VERSION_UNDEFINED](FeatureInfo.md) Default value for [reqGlEsVersion](FeatureInfo.md); |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FeatureInfo](FeatureInfo.md))`()` <br /> |
| [FeatureInfo](FeatureInfo.md))`(`orig:` ` [FeatureInfo](FeatureInfo.md)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](FeatureInfo.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getGlEsVersion](FeatureInfo.md))`()` This method extracts the major and minor version of reqGLEsVersion attribute and returns it as a string. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](FeatureInfo.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](FeatureInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `parcelableFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [FeatureInfo](FeatureInfo.md)!\> | [CREATOR](FeatureInfo.md) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [flags](FeatureInfo.md) Additional flags. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [name](FeatureInfo.md) The name of this feature, for example "android. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [reqGlEsVersion](FeatureInfo.md) The GLES version used by an application. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [version](FeatureInfo.md) If this object represents a feature supported by a device, this is the maximum version of this feature supported by the device. |

## Constants

### FLAG_REQUIRED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_REQUIRED: Int
```

Set on [flags](FeatureInfo.md) if this feature has been required by the application. 

 Value: 1

### GL_ES_VERSION_UNDEFINED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GL_ES_VERSION_UNDEFINED: Int
```

Default value for [reqGlEsVersion](FeatureInfo.md); 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

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

Additional flags. May be zero or more of [FLAG_REQUIRED](FeatureInfo.md). 

### name

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var name: String!
```

The name of this feature, for example "android.hardware.camera". If this is null, then this is an OpenGL ES version feature as described in [reqGlEsVersion](FeatureInfo.md). 

### reqGlEsVersion

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var reqGlEsVersion: Int
```

The GLES version used by an application. The upper order 16 bits represent the major version and the lower order 16 bits the minor version. Only valid if [name](FeatureInfo.md) is null. 

### version

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var version: Int
```

If this object represents a feature supported by a device, this is the maximum version of this feature supported by the device. The device implicitly supports all older versions of this feature.

If this object represents a feature requested by an app, this is the minimum version of the feature required by the app.

When a feature version is undefined by a device, it's assumed to be version 0.
