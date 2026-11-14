Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrustedPresentationThresholds

```
class TrustedPresentationThresholds : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.window.TrustedPresentationThresholds](TrustedPresentationThresholds.md) |

Threshold values that are sent with android.view.WindowManager#registerTrustedPresentationListener(IBinder,android.window.TrustedPresentationThresholds,Executor,Consumer)

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds#SIGNAL_MODE_STRICT_OCCLUSION:kotlin.Int` Only signal occlusion when the system is certain that the window is obscured by truly opaque windows. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds#SIGNAL_MODE_TRUSTED_PRESENTATION:kotlin.Int` Signal occlusion based on the trusted presentation thresholds. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| TrustedPresentationThresholds Creates a new TrustedPresentationThresholds. |
| TrustedPresentationThresholds Creates a new TrustedPresentationThresholds. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getMinAlpha The min alpha the Window is required to have to be considered inside the threshold. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | getMinFractionRendered The min fraction of the Window that was presented to the user to be considered inside the threshold. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSignalMode Returns the mode that determines when to signal occlusion. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getStabilityRequirementMillis The time in milliseconds required for the Window to be in the threshold. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TrustedPresentationThresholds](TrustedPresentationThresholds.md)!\> | `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### SIGNAL_MODE_STRICT_OCCLUSION

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNAL_MODE_STRICT_OCCLUSION: Int
```

Only signal occlusion when the system is certain that the window is obscured by truly opaque windows.

 Value: 1

### SIGNAL_MODE_TRUSTED_PRESENTATION

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SIGNAL_MODE_TRUSTED_PRESENTATION: Int
```

Signal occlusion based on the trusted presentation thresholds.

 Value: 0

## Public constructors

### TrustedPresentationThresholds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TrustedPresentationThresholds(
    minAlpha: Float, 
    minFractionRendered: Float, 
    stabilityRequirementMs: Int)
```

Creates a new TrustedPresentationThresholds. The default signal mode is `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds#SIGNAL_MODE_TRUSTED_PRESENTATION:kotlin.Int`.

| Parameters ||
|---|---|
| `minAlpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The min alpha the Window is required to have to be considered inside the threshold. Value is between 0.0f and 1.0f inclusive |
| `minFractionRendered` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The min fraction of the Window that was presented to the user to be considered inside the threshold. Value is between 0.0f and 1.0f inclusive |
| `stabilityRequirementMs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The time in milliseconds required for the Window to be in the threshold. Value is 1 or greater |
| --- | --- |

### TrustedPresentationThresholds

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TrustedPresentationThresholds(
    minAlpha: Float, 
    minFractionRendered: Float, 
    stabilityRequirementMs: Int, 
    signalMode: Int)
```

Creates a new TrustedPresentationThresholds.

| Parameters ||
|---|---|
| `minAlpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The min alpha the Window is required to have to be considered inside the threshold. Value is between 0.0f and 1.0f inclusive |
| `minFractionRendered` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The min fraction of the Window that was presented to the user to be considered inside the threshold. Value is between 0.0f and 1.0f inclusive |
| `stabilityRequirementMs` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The time in milliseconds required for the Window to be in the threshold. Value is 1 or greater |
| --- | --- |
| `signalMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The mode that determines when to signal occlusion. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds#SIGNAL_MODE_TRUSTED_PRESENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds#SIGNAL_MODE_STRICT_OCCLUSION:kotlin.Int` |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getMinAlpha

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinAlpha(): Float
```

The min alpha the Window is required to have to be considered inside the threshold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 1.0f inclusive |

### getMinFractionRendered

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMinFractionRendered(): Float
```

The min fraction of the Window that was presented to the user to be considered inside the threshold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | Value is between 0.0f and 1.0f inclusive |

### getSignalMode

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSignalMode(): Int
```

Returns the mode that determines when to signal occlusion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds#SIGNAL_MODE_TRUSTED_PRESENTATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/window/TrustedPresentationThresholds#SIGNAL_MODE_STRICT_OCCLUSION:kotlin.Int` |

### getStabilityRequirementMillis

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStabilityRequirementMillis(): Int
```

The time in milliseconds required for the Window to be in the threshold.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is 1 or greater |

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

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
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TrustedPresentationThresholds!>
```
