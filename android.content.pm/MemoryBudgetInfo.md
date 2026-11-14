Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MemoryBudgetInfo

```
class MemoryBudgetInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.pm.MemoryBudgetInfo](https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#) |

Memory budget information for an application. entries are retrieved from \<memory-budget\> entries in an application's manifest, and can be obtained through `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager#getMemoryBudgets(android.content.pm.ApplicationInfo)`.

A `MemoryBudgetInfo` that is declared in the Android manifest sets a ceiling on the memory available to the package or to a process within the package. `MemoryBudgetInfo` declarations may appear at the application level and at the process level. The two are independent and neither overrides the other. In practice, however, the smaller budget dominates.

Every `MemoryBudgetInfo` has a state and a feature; these two attributes determine if and when the `MemoryBudgetInfo` is applicable.

- The state is the operational state of the process or the application, and is one of Foreground, Perceptible, or Background.
- The feature selects for device form-factor and is one of Unspecified, TV, Auto, and Watch.

A `MemoryBudgetInfo` is *applicable* to a process if its feature is Unspecified or if its feature matches the device's form-factor. A `MemoryBudgetInfo` *applies* to a process if it is applicable to the process and the `MemoryBudgetInfo` state is less than or equal to the operational state of the process. Applications also have state, which is roughly the lowest state of any process running in the application.

A `MemoryBudgetInfo` declares an upper bound on the amount of memory the process or application may use. The upper bound is computed from three factors:

- `maxMb` is a baseline amount of memory, expressed in MiB. This must be positive.
- `additionalBytesPerPixel` is a scaling factor: bytes per display pixel. This must be non-negative and defaults to zero.
- `additionalMbPerDensity` is a scaling factor: MiB times display density. This must be non-negative and defaults to zero.

The actual limit is calculated as the `maxMb` value plus the scale factors applied to the default display of the device.

If a process RSS exceeds its declared budget then the kernel will force it to drop memory. This usually means dropping file cache pages but it may also mean that some memory will be moved to swap. In most cases this happens without any impact on the process, but if the process is actively using more memory than the budget limit, the process will slow down as pages are swapped out and then back in. In the limit, the process may ANR.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#FEATURE_AUTOMOTIVE:kotlin.Int` Indicates that this `MemoryBudgetInfo` applies to the automotive form factor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#FEATURE_LEANBACK:kotlin.Int` Indicates that this `MemoryBudgetInfo` applies to the TV form factor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#FEATURE_UNSPECIFIED:kotlin.Int` Indicates that this `MemoryBudgetInfo` is generic, and can apply to any form factor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#FEATURE_WATCH:kotlin.Int` Indicates that this `MemoryBudgetInfo` applies to the watch form factor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#STATE_BACKGROUND:kotlin.Int` Indicates that this `MemoryBudgetInfo` can apply to a process that is in the background. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#STATE_FOREGROUND:kotlin.Int` Indicates that this `MemoryBudgetInfo` can apply to a process that is in the foreground (or in a less important state). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#STATE_PERCEPTIBLE:kotlin.Int` Indicates that this `MemoryBudgetInfo` can apply to a process that is perceptible (or in a less important state). |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#getAdditionalBytesPerDisplayPixel()()` Returns the additional bytes per pixel that this `MemoryBudgetInfo`'s limit will be raised by. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#getAdditionalMbPerDensity()()` Returns the additional memory (in MiB) that this `MemoryBudgetInfo`'s limit will be raised by, based on the screen density of the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#getFeature()()` Returns the form factor to which this `MemoryBudgetInfo` applies. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#getMaxMb()()` Returns the memory limit (in MiB) that this `MemoryBudgetInfo` represents. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#getState()()` Returns the process state in which this `MemoryBudgetInfo` applies. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MemoryBudgetInfo](https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#)!\> | `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### FEATURE_AUTOMOTIVE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_AUTOMOTIVE: Int
```

Indicates that this `MemoryBudgetInfo` applies to the automotive form factor.

 Value: 1

### FEATURE_LEANBACK

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_LEANBACK: Int
```

Indicates that this `MemoryBudgetInfo` applies to the TV form factor.

 Value: 2

### FEATURE_UNSPECIFIED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_UNSPECIFIED: Int
```

Indicates that this `MemoryBudgetInfo` is generic, and can apply to any form factor. This is the default if "feature" is not specified in the manifest.

 Value: 0

### FEATURE_WATCH

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FEATURE_WATCH: Int
```

Indicates that this `MemoryBudgetInfo` applies to the watch form factor.

 Value: 3

### STATE_BACKGROUND

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_BACKGROUND: Int
```

Indicates that this `MemoryBudgetInfo` can apply to a process that is in the background.

 Value: 300

### STATE_FOREGROUND

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_FOREGROUND: Int
```

Indicates that this `MemoryBudgetInfo` can apply to a process that is in the foreground (or in a less important state). This is the default if "state" is not specified in the manifest.

 Value: 100

### STATE_PERCEPTIBLE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_PERCEPTIBLE: Int
```

Indicates that this `MemoryBudgetInfo` can apply to a process that is perceptible (or in a less important state).

 Value: 200

## Public methods

### describeContents

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAdditionalBytesPerDisplayPixel

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAdditionalBytesPerDisplayPixel(): Long
```

Returns the additional bytes per pixel that this `MemoryBudgetInfo`'s limit will be raised by.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The additionalBytesPerDisplayPixel attribute. Value is between 0 and #MAX_ADDITIONAL_BYTES_PER_DISPLAY_PIXEL inclusive |

### getAdditionalMbPerDensity

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAdditionalMbPerDensity(): Long
```

Returns the additional memory (in MiB) that this `MemoryBudgetInfo`'s limit will be raised by, based on the screen density of the device. The formula used for calculating the additional memory is (N \* { ldpi=0.75, mdpi=1.0, hdpi=1.5, xhdpi=2... }).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The additionalMbPerDensity attribute. Value is between 0 and #MAX_ADDITIONAL_MB_PER_DENSITY inclusive |

### getFeature

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFeature(): Int
```

Returns the form factor to which this `MemoryBudgetInfo` applies.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The form factor to which this `MemoryBudgetInfo` applies. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#FEATURE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#FEATURE_AUTOMOTIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#FEATURE_LEANBACK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#FEATURE_WATCH:kotlin.Int` |

### getMaxMb

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxMb(): Long
```

Returns the memory limit (in MiB) that this `MemoryBudgetInfo` represents.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The memory limit (in MiB) that this `MemoryBudgetInfo` represents. Value is between 1 and #MAX_MAXMB inclusive |

### getState

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getState(): Int
```

Returns the process state in which this `MemoryBudgetInfo` applies.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The process state in which this `MemoryBudgetInfo` applies. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#STATE_FOREGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#STATE_PERCEPTIBLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/content/pm/MemoryBudgetInfo#STATE_BACKGROUND:kotlin.Int` |

### hashCode

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### toString

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<MemoryBudgetInfo!>
```
