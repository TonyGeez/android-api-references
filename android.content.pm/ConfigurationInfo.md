Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConfigurationInfo

Kotlin | [Java](../android/content/pm/ConfigurationInfo.md)
| --- | --- |

```
open class ConfigurationInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.pm.ConfigurationInfo](../android/content/pm/ConfigurationInfo.md) |

Information you can retrieve about hardware configuration preferences declared by an application. This corresponds to information collected from the AndroidManifest.xml's \<uses-configuration\> and \<uses-feature\> tags.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#GL_ES_VERSION_UNDEFINED:kotlin.Int` Default value for `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqGlEsVersion:kotlin.Int`; |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#INPUT_FEATURE_FIVE_WAY_NAV:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqInputFeatures:kotlin.Int`: if set, indicates that the application requires a five way navigation device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#INPUT_FEATURE_HARD_KEYBOARD:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqInputFeatures:kotlin.Int`: if set, indicates that the application requires a hard keyboard |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#ConfigurationInfo()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#ConfigurationInfo(android.content.pm.ConfigurationInfo)(orig: https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#!)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#getGlEsVersion()()` This method extracts the major and minor version of reqGLEsVersion attribute and returns it as a string. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#toString()()` Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, parcelableFlags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ConfigurationInfo](../android/content/pm/ConfigurationInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#CREATOR:android.os.Parcelable.Creator` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqGlEsVersion:kotlin.Int` The GLES version used by an application. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqInputFeatures:kotlin.Int` Flags associated with the input features. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqKeyboardType:kotlin.Int` Application's input method preference. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqNavigation:kotlin.Int` A flag indicating whether any keyboard is available. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqTouchScreen:kotlin.Int` The kind of touch screen attached to the device. |
| --- | --- |

## Constants

### GL_ES_VERSION_UNDEFINED

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val GL_ES_VERSION_UNDEFINED: Int
```

Default value for `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqGlEsVersion:kotlin.Int`;

 Value: 0

### INPUT_FEATURE_FIVE_WAY_NAV

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INPUT_FEATURE_FIVE_WAY_NAV: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqInputFeatures:kotlin.Int`: if set, indicates that the application requires a five way navigation device

 Value: 2

### INPUT_FEATURE_HARD_KEYBOARD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INPUT_FEATURE_HARD_KEYBOARD: Int
```

Value for `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#reqInputFeatures:kotlin.Int`: if set, indicates that the application requires a hard keyboard

 Value: 1

## Public constructors

### ConfigurationInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConfigurationInfo()
```

### ConfigurationInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConfigurationInfo(orig: ConfigurationInfo!)
```

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getGlEsVersion

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGlEsVersion(): String!
```

This method extracts the major and minor version of reqGLEsVersion attribute and returns it as a string. Say reqGlEsVersion value of 0x00010002 is returned as 1.2

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | String representation of the reqGlEsVersion attribute |

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    parcelableFlags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ConfigurationInfo!>
```

### reqGlEsVersion

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var reqGlEsVersion: Int
```

The GLES version used by an application. The upper order 16 bits represent the major version and the lower order 16 bits the minor version.

### reqInputFeatures

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var reqInputFeatures: Int
```

Flags associated with the input features. Any combination of `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#INPUT_FEATURE_HARD_KEYBOARD:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/pm/ConfigurationInfo#INPUT_FEATURE_FIVE_WAY_NAV:kotlin.Int`

### reqKeyboardType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var reqKeyboardType: Int
```

Application's input method preference. One of: `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#KEYBOARD_UNDEFINED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#KEYBOARD_NOKEYS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#KEYBOARD_QWERTY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#KEYBOARD_12KEY:kotlin.Int`

### reqNavigation

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var reqNavigation: Int
```

A flag indicating whether any keyboard is available. one of: `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#NAVIGATION_UNDEFINED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#NAVIGATION_DPAD:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#NAVIGATION_TRACKBALL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#NAVIGATION_WHEEL:kotlin.Int`

### reqTouchScreen

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var reqTouchScreen: Int
```

The kind of touch screen attached to the device. One of: `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#TOUCHSCREEN_NOTOUCH:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#TOUCHSCREEN_STYLUS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#TOUCHSCREEN_FINGER:kotlin.Int`.
