# VirtualDisplayConfig

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualDisplayConfig

Kotlin| [Java](VirtualDisplayConfig.md) 
| --- | --- |

```
class VirtualDisplayConfig : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.display.VirtualDisplayConfig](VirtualDisplayConfig.md) |

Holds configuration used to create [VirtualDisplay](VirtualDisplay.md) instances.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [BrightnessListener](../android/hardware/display/VirtualDisplayConfig.BrightnessListener.md) Listener for display brightness changes. |
| | [Builder](../android/hardware/display/VirtualDisplayConfig.Builder.md) A builder for [VirtualDisplayConfig](VirtualDisplayConfig.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](VirtualDisplayConfig.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](VirtualDisplayConfig.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDefaultBrightness](VirtualDisplayConfig.md))`()` Returns the default brightness of the display. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDensityDpi](VirtualDisplayConfig.md))`()` Returns the density of the virtual display in dpi. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDimBrightness](VirtualDisplayConfig.md))`()` Returns the dim brightness of the display. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getDisplayCategories](VirtualDisplayConfig.md))`()` Returns the display categories. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](VirtualDisplayConfig.md))`()` Returns the virtual display flags. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](VirtualDisplayConfig.md))`()` Returns the height of the virtual display in pixels. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](VirtualDisplayConfig.md))`()` Returns the name of the virtual display. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getRequestedRefreshRate](VirtualDisplayConfig.md))`()` Returns the refresh rate of a virtual display in frames per second, or zero if it is using a default refresh rate chosen by the system. |
| [Surface](../android.view/Surface.md)? | [getSurface](VirtualDisplayConfig.md))`()` Returns the surface to which the content of the virtual display should be rendered, if any. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](VirtualDisplayConfig.md))`()` Returns the width of the virtual display in pixels. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](VirtualDisplayConfig.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](VirtualDisplayConfig.md))`()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](VirtualDisplayConfig.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [VirtualDisplayConfig](VirtualDisplayConfig.md)!\> | [CREATOR](VirtualDisplayConfig.md) <br /> |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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

- [android.hardware.display.VirtualDisplayConfig.Builder#setDefaultBrightness(float)](../android/hardware/display/VirtualDisplayConfig.Builder.md)) 

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

- [android.hardware.display.VirtualDisplayConfig.Builder#setDimBrightness(float)](../android/hardware/display/VirtualDisplayConfig.Builder.md)) 

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

- [android.hardware.display.VirtualDisplayConfig.Builder#setDisplayCategories](../android/hardware/display/VirtualDisplayConfig.Builder.md)) 

### getFlags

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Returns the virtual display flags. 
**See Also**

- [android.hardware.display.VirtualDisplayConfig.Builder#setFlags](../android/hardware/display/VirtualDisplayConfig.Builder.md)) 

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

- [android.hardware.display.VirtualDisplayConfig.Builder#setRequestedRefreshRate](../android/hardware/display/VirtualDisplayConfig.Builder.md)) 

### getSurface

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSurface(): Surface?
```

Returns the surface to which the content of the virtual display should be rendered, if any.

| Return ||
|---------------------------------------------------------------------------------------|--------------------------|
| [Surface](../android.view/Surface.md)? | This value may be`null`. |

**See Also**

- [android.hardware.display.VirtualDisplayConfig.Builder#setSurface](../android/hardware/display/VirtualDisplayConfig.Builder.md)) 

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<VirtualDisplayConfig!>
```
