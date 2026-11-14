# BluetoothCodecStatus

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothCodecStatus

Kotlin | [Java](https://developer.android.com/reference/android/bluetooth/BluetoothCodecStatus "View this page in Java") 
| --- | --- |

```
class BluetoothCodecStatus : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothCodecStatus](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#) |

Represents the codec status (configuration and capability) for a Bluetooth A2DP source device.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus.Builder) Builder for [BluetoothCodecStatus](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#). |

| Constants ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CODEC_STATUS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#EXTRA_CODEC_STATUS:kotlin.String) Extra for the codec configuration intents of the individual profiles. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [BluetoothCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecConfig)? | [getCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#getCodecConfig())`()` Returns the current codec configuration. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecConfig)!\> | [getCodecsLocalCapabilities](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#getCodecsLocalCapabilities())`()` Returns the codecs local capabilities. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecConfig)!\> | [getCodecsSelectableCapabilities](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#getCodecsSelectableCapabilities())`()` Returns the codecs selectable capabilities. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#hashCode())`()` Returns a hash based on the codec config and local capabilities. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCodecConfigSelectable](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#isCodecConfigSelectable(android.bluetooth.BluetoothCodecConfig))`(`codecConfig:` ` [BluetoothCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecConfig)?`)` Checks whether the codec config matches the selectable capabilities. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#toString())`()` Returns a [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) that describes each BluetoothCodecStatus parameter current value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flattens the object to a parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BluetoothCodecStatus](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecStatus#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### EXTRA_CODEC_STATUS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CODEC_STATUS: String
```

Extra for the codec configuration intents of the individual profiles.

This extra represents the current codec status of the A2DP profile. 

 Value: "android.bluetooth.extra.CODEC_STATUS"

## Public methods

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getCodecConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecConfig(): BluetoothCodecConfig?
```

Returns the current codec configuration.

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------|
| [BluetoothCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecConfig)? | This value may be `null`. |

### getCodecsLocalCapabilities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecsLocalCapabilities(): MutableList<BluetoothCodecConfig!>
```

Returns the codecs local capabilities.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecConfig)!> | This value cannot be `null`. |

### getCodecsSelectableCapabilities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCodecsSelectableCapabilities(): MutableList<BluetoothCodecConfig!>
```

Returns the codecs selectable capabilities.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecConfig)!> | This value cannot be `null`. |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash based on the codec config and local capabilities.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isCodecConfigSelectable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCodecConfigSelectable(codecConfig: BluetoothCodecConfig?): Boolean
```

Checks whether the codec config matches the selectable capabilities. Any parameters of the codec config with NONE value will be considered a wildcard matching.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `codecConfig` | [BluetoothCodecConfig](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCodecConfig)?: the codec config to compare against This value may be `null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the codec config matches, `false` otherwise |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) that describes each BluetoothCodecStatus parameter current value.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flattens the object to a parcel.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written |
| `out` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The Parcel in which the object should be written This value cannot be `null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BluetoothCodecStatus!>
```
