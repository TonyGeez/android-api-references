Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationCapability

```
class TranslationCapability : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.translation.TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#) |

Capability class holding information for a pair of `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec`s.

Holds information and limitations on how to create a `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext` which can be used by `https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#createOnDeviceTranslator(android.view.translation.TranslationContext,%20java.util.concurrent.Executor,%20java.util.function.Consumer)`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_AVAILABLE_TO_DOWNLOAD:kotlin.Int` The translation service supports translation between the source and target specs, and it is ready to be downloaded onto the device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_DOWNLOADING:kotlin.Int` The translation service supports translation between the source and target specs, and it is being downloaded onto the device currently. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_NOT_AVAILABLE:kotlin.Int` The translation service does not support translation between the source and target specs. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_ON_DEVICE:kotlin.Int` The translation service supports translation between the source and target specs, and it is downloaded and ready to use on device. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

<br />

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

<br />

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [TranslationSpec](https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#getSourceSpec()()` `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec` describing the source data specs for this capability. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#getState()()` The state of translation readiness between `mSourceSpec` and `mTargetSpec`. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#getSupportedTranslationFlags()()` Translation flags for settings that are supported by the `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#` between the `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec`s provided in this capability. |
| [TranslationSpec](https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#getTargetSpec()()` `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec` describing the target data specs for this capability. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#isUiTranslationEnabled()()` Whether ui translation for the source-target `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec`s is enabled. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TranslationCapability](https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#)!\> | `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### STATE_AVAILABLE_TO_DOWNLOAD

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_AVAILABLE_TO_DOWNLOAD: Int
```

The translation service supports translation between the source and target specs, and it is ready to be downloaded onto the device. 

Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_AVAILABLE_TO_DOWNLOAD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_DOWNLOADING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_ON_DEVICE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_NOT_AVAILABLE:kotlin.Int`

<br />

 Value: 1

### STATE_DOWNLOADING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_DOWNLOADING: Int
```

The translation service supports translation between the source and target specs, and it is being downloaded onto the device currently. 

Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_AVAILABLE_TO_DOWNLOAD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_DOWNLOADING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_ON_DEVICE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_NOT_AVAILABLE:kotlin.Int`

<br />

 Value: 2

### STATE_NOT_AVAILABLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_NOT_AVAILABLE: Int
```

The translation service does not support translation between the source and target specs.

Note: This state is not returned from calling `https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#getOnDeviceTranslationCapabilities(kotlin.Int,%20kotlin.Int)`. This state will only appear as part of capability updates from `https://developer.android.com/reference/kotlin/android/view/translation/TranslationManager#addOnDeviceTranslationCapabilityUpdateListener(java.util.concurrent.Executor,%20java.util.function.Consumer)` if existing support was dropped.
. 
Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_AVAILABLE_TO_DOWNLOAD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_DOWNLOADING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_ON_DEVICE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_NOT_AVAILABLE:kotlin.Int`

 Value: 4

### STATE_ON_DEVICE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_ON_DEVICE: Int
```

The translation service supports translation between the source and target specs, and it is downloaded and ready to use on device. 

Value is one of the following:

- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_AVAILABLE_TO_DOWNLOAD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_DOWNLOADING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_ON_DEVICE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_NOT_AVAILABLE:kotlin.Int`

<br />

 Value: 3

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getSourceSpec

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSourceSpec(): TranslationSpec
```

`https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec` describing the source data specs for this capability.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec` | This value cannot be `null`. |

### getState

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getState(): Int
```

The state of translation readiness between `mSourceSpec` and `mTargetSpec`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_AVAILABLE_TO_DOWNLOAD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_DOWNLOADING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_ON_DEVICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#STATE_NOT_AVAILABLE:kotlin.Int` |

### getSupportedTranslationFlags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSupportedTranslationFlags(): Int
```

Translation flags for settings that are supported by the `https://developer.android.com/reference/kotlin/android/view/translation/TranslationCapability#` between the `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec`s provided in this capability.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_LOW_LATENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_TRANSLITERATION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/translation/TranslationContext#FLAG_DEFINITIONS:kotlin.Int` |

### getTargetSpec

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTargetSpec(): TranslationSpec
```

`https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec` describing the target data specs for this capability.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec` | This value cannot be `null`. |

### isUiTranslationEnabled

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isUiTranslationEnabled(): Boolean
```

Whether ui translation for the source-target `https://developer.android.com/reference/kotlin/android/view/translation/TranslationSpec`s is enabled.

Translation service will still support translation requests for this capability.

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TranslationCapability!>
```
