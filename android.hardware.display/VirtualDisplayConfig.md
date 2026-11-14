# VirtualDisplayConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualDisplayConfig

Kotlin| [Java](https://developer.android.com/reference/android/hardware/display/VirtualDisplayConfig "View this page in Java") 

```
class VirtualDisplayConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.display.VirtualDisplayConfig](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#) |

Holds configuration used to create [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay) instances.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [BrightnessListener](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig.BrightnessListener) Listener for display brightness changes. |
| | [Builder](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig.Builder) A builder for [VirtualDisplayConfig](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDefaultBrightness](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getDefaultBrightness())`()` Returns the default brightness of the display. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDensityDpi](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getDensityDpi())`()` Returns the density of the virtual display in dpi. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDimBrightness](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getDimBrightness())`()` Returns the dim brightness of the display. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDisplayCategories](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getDisplayCategories())`()` Returns the display categories. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getFlags())`()` Returns the virtual display flags. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getHeight())`()` Returns the height of the virtual display in pixels. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getName())`()` Returns the name of the virtual display. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRequestedRefreshRate](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getRequestedRefreshRate())`()` Returns the refresh rate of a virtual display in frames per second, or zero if it is using a default refresh rate chosen by the system. |
| [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)? | [getSurface](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getSurface())`()` Returns the surface to which the content of the virtual display should be rendered, if any. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#getWidth())`()` Returns the width of the virtual display in pixels. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#toString())`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [VirtualDisplayConfig](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDefaultBrightness

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultBrightness(): Float
```

Returns the default brightness of the display.

Value of`0.0`indicates the minimum supported brightness and value of`1.0`indicates the maximum supported brightness.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is between 0.0f and 1.0f inclusive |

**See Also**

- [android.hardware.display.VirtualDisplayConfig.Builder#setDefaultBrightness(float)](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig.Builder#setDefaultBrightness(kotlin.Float)) 

### getDensityDpi

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDensityDpi(): Int
```

Returns the density of the virtual display in dpi. 

### getDimBrightness

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDimBrightness(): Float
```

Returns the dim brightness of the display.

Value of`0.0`indicates the minimum supported brightness and value of`1.0`indicates the maximum supported brightness.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is between 0.0f and 1.0f inclusive |

**See Also**

- [android.hardware.display.VirtualDisplayConfig.Builder#setDimBrightness(float)](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig.Builder#setDimBrightness(kotlin.Float)) 

### getDisplayCategories

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDisplayCategories(): MutableSet<String!>
```

Returns the display categories.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

**See Also**

- [android.hardware.display.VirtualDisplayConfig.Builder#setDisplayCategories](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig.Builder#setDisplayCategories(kotlin.collections.MutableSet)) 

### getFlags

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Returns the virtual display flags. 
**See Also**

- [android.hardware.display.VirtualDisplayConfig.Builder#setFlags](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig.Builder#setFlags(kotlin.Int)) 

### getHeight

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHeight(): Int
```

Returns the height of the virtual display in pixels. 

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns the name of the virtual display.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getRequestedRefreshRate

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestedRefreshRate(): Float
```

Returns the refresh rate of a virtual display in frames per second, or zero if it is using a default refresh rate chosen by the system. 
**See Also**

- [android.hardware.display.VirtualDisplayConfig.Builder#setRequestedRefreshRate](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig.Builder#setRequestedRefreshRate(kotlin.Float)) 

### getSurface

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSurface(): Surface?
```

Returns the surface to which the content of the virtual display should be rendered, if any.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------|
| [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#)? | This value may be`null`. |

**See Also**

- [android.hardware.display.VirtualDisplayConfig.Builder#setSurface](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplayConfig.Builder#setSurface(android.view.Surface)) 

### getWidth

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWidth(): Int
```

Returns the width of the virtual display in pixels. 

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<VirtualDisplayConfig!>
```
