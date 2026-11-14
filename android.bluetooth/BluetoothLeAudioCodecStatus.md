# BluetoothLeAudioCodecStatus

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothLeAudioCodecStatus

Kotlin| [Java](BluetoothLeAudioCodecStatus.md) 
| --- | --- |

```
class BluetoothLeAudioCodecStatus : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothLeAudioCodecStatus](BluetoothLeAudioCodecStatus.md) |

Represents the codec status (configuration and capability) for a Bluetooth Le Audio source device.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_LE_AUDIO_CODEC_STATUS](BluetoothLeAudioCodecStatus.md) Extra for the codec configuration intents of the individual profiles. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothLeAudioCodecStatus](BluetoothLeAudioCodecStatus.md))`(`inputCodecConfig:` ` [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)?`, `outputCodecConfig:` ` [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)?`, `inputCodecsLocalCapabilities:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!>`, `outputCodecsLocalCapabilities:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!>`, `inputCodecsSelectableCapabilities:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!>`, `outputCodecsSelectableCapabilities:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!>`)` Represents the codec status for a Bluetooth LE Audio source device. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](BluetoothLeAudioCodecStatus.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](BluetoothLeAudioCodecStatus.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)? | [getInputCodecConfig](BluetoothLeAudioCodecStatus.md))`()` Returns the current Input codec configuration. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!\> | [getInputCodecLocalCapabilities](BluetoothLeAudioCodecStatus.md))`()` Returns the input codecs local capabilities. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!\> | [getInputCodecSelectableCapabilities](BluetoothLeAudioCodecStatus.md))`()` Returns the Input codecs selectable capabilities. |
| [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)? | [getOutputCodecConfig](BluetoothLeAudioCodecStatus.md))`()` Returns the current Output codec configuration. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!\> | [getOutputCodecLocalCapabilities](BluetoothLeAudioCodecStatus.md))`()` Returns the output codecs local capabilities. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!\> | [getOutputCodecSelectableCapabilities](BluetoothLeAudioCodecStatus.md))`()` Returns the Output codecs selectable capabilities. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](BluetoothLeAudioCodecStatus.md))`()` Returns a hash based on the codec config and local capabilities. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInputCodecConfigSelectable](BluetoothLeAudioCodecStatus.md))`(`codecConfig:` ` [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)?`)` Checks whether the Input codec config matches the selectable capabilities. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOutputCodecConfigSelectable](BluetoothLeAudioCodecStatus.md))`(`codecConfig:` ` [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)?`)` Checks whether the Output codec config matches the selectable capabilities. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](BluetoothLeAudioCodecStatus.md))`()` Returns a [String](../java.lang/String.md) that describes each BluetoothLeAudioCodecStatus parameter current value. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](BluetoothLeAudioCodecStatus.md))`(`out:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flattens the object to a parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BluetoothLeAudioCodecStatus](BluetoothLeAudioCodecStatus.md)!\> | [CREATOR](BluetoothLeAudioCodecStatus.md) [Parcelable.Creator](../android/os/Parcelable.Creator.md) interface implementation. |

## Constants

### EXTRA_LE_AUDIO_CODEC_STATUS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_LE_AUDIO_CODEC_STATUS: String
```

Extra for the codec configuration intents of the individual profiles.

This extra represents the current codec status of the Le Audio profile. 

 Value: "android.bluetooth.extra.LE_AUDIO_CODEC_STATUS"

## Public constructors

### BluetoothLeAudioCodecStatus

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BluetoothLeAudioCodecStatus(
    inputCodecConfig: BluetoothLeAudioCodecConfig?, 
    outputCodecConfig: BluetoothLeAudioCodecConfig?, 
    inputCodecsLocalCapabilities: MutableList<BluetoothLeAudioCodecConfig!>, 
    outputCodecsLocalCapabilities: MutableList<BluetoothLeAudioCodecConfig!>, 
    inputCodecsSelectableCapabilities: MutableList<BluetoothLeAudioCodecConfig!>, 
    outputCodecsSelectableCapabilities: MutableList<BluetoothLeAudioCodecConfig!>)
```

Represents the codec status for a Bluetooth LE Audio source device.

| Parameters ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputCodecConfig` | [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)?:the current input codec configuration. This value may be`null`. |
| `outputCodecConfig` | [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)?:the current output codec configuration. This value may be`null`. |
| `inputCodecsLocalCapabilities` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!\>:the local input codecs capabilities. This value cannot be`null`. |
| --- | --- |
| `outputCodecsLocalCapabilities` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!\>:the local output codecs capabilities. This value cannot be`null`. |
| `inputCodecsSelectableCapabilities` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!\>:the selectable input codecs capabilities. This value cannot be`null`. |
| `outputCodecsSelectableCapabilities` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!\>:the selectable output codecs capabilities. This value cannot be`null`. |
| --- | --- |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 |

### equals

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getInputCodecConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputCodecConfig(): BluetoothLeAudioCodecConfig?
```

Returns the current Input codec configuration.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)? | The current input codec config. This value may be`null`. |

### getInputCodecLocalCapabilities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputCodecLocalCapabilities(): MutableList<BluetoothLeAudioCodecConfig!>
```

Returns the input codecs local capabilities.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!> | The list of codec config that supported by the local system. This value cannot be`null`. |

### getInputCodecSelectableCapabilities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputCodecSelectableCapabilities(): MutableList<BluetoothLeAudioCodecConfig!>
```

Returns the Input codecs selectable capabilities.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!> | The list of codec config that supported by both of the local system and remote devices. This value cannot be`null`. |

### getOutputCodecConfig

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputCodecConfig(): BluetoothLeAudioCodecConfig?
```

Returns the current Output codec configuration.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)? | The current output codec config. This value may be`null`. |

### getOutputCodecLocalCapabilities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputCodecLocalCapabilities(): MutableList<BluetoothLeAudioCodecConfig!>
```

Returns the output codecs local capabilities.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!> | The list of codec config that supported by the local system. This value cannot be`null`. |

### getOutputCodecSelectableCapabilities

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputCodecSelectableCapabilities(): MutableList<BluetoothLeAudioCodecConfig!>
```

Returns the Output codecs selectable capabilities.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)!> | The list of codec config that supported by both of the local system and remote devices. This value cannot be`null`. |

### hashCode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash based on the codec config and local capabilities.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isInputCodecConfigSelectable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInputCodecConfigSelectable(codecConfig: BluetoothLeAudioCodecConfig?): Boolean
```

Checks whether the Input codec config matches the selectable capabilities. Any parameters of the codec config with NONE value will be considered a wildcard matching.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `codecConfig` | [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)?:the codec config to compare against This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the codec config matches,`false`otherwise |

### isOutputCodecConfigSelectable

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isOutputCodecConfigSelectable(codecConfig: BluetoothLeAudioCodecConfig?): Boolean
```

Checks whether the Output codec config matches the selectable capabilities. Any parameters of the codec config with NONE value will be considered a wildcard matching.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `codecConfig` | [BluetoothLeAudioCodecConfig](BluetoothLeAudioCodecConfig.md)?:the codec config to compare against This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the codec config matches,`false`otherwise |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a [String](../java.lang/String.md) that describes each BluetoothLeAudioCodecStatus parameter current value.

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written |
| `out` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written This value cannot be`null`. |
| --- | --- |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BluetoothLeAudioCodecStatus!>
```

[Parcelable.Creator](../android/os/Parcelable.Creator.md) interface implementation.
