Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

# PhotoPickerUiCustomizationParams

```
class PhotoPickerUiCustomizationParams : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.photopicker.PhotoPickerUiCustomizationParams](https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#) |

Defines UI customization options for the system's Photo Picker interface.

This immutable class allows an application to specify visual preferences to optimize the user experience within the picker.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams.Builder` A builder class used to construct and validate an immutable `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#` object. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#ASPECT_RATIO_PORTRAIT_9_16:kotlin.Int` Aspect ratio option requesting portrait 9:16 sizing for the thumbnails within the media grid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#ASPECT_RATIO_SQUARE_1_1:kotlin.Int` Aspect ratio option requesting square 1:1 thumbnail sizing within the media grid. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#ASPECT_RATIO_UNDEFINED:kotlin.Int` Aspect ratio option sent to photo picker when no aspect ratio is set by the calling app. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#getAspectRatio()()` Returns the constant representing the aspect ratio currently configured for thumbnail sizing within the Photo Picker's media grid. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PhotoPickerUiCustomizationParams](https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#)!\> | `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ASPECT_RATIO_PORTRAIT_9_16

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
static val ASPECT_RATIO_PORTRAIT_9_16: Int
```

Aspect ratio option requesting portrait 9:16 sizing for the thumbnails within the media grid.

 Value: 1

### ASPECT_RATIO_SQUARE_1_1

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
static val ASPECT_RATIO_SQUARE_1_1: Int
```

Aspect ratio option requesting square 1:1 thumbnail sizing within the media grid.

 Value: 0

### ASPECT_RATIO_UNDEFINED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
static val ASPECT_RATIO_UNDEFINED: Int
```

Aspect ratio option sent to photo picker when no aspect ratio is set by the calling app.

 Value: -1

## Public methods

### describeContents

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAspectRatio

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
fun getAspectRatio(): Int
```

Returns the constant representing the aspect ratio currently configured for thumbnail sizing within the Photo Picker's media grid. (e.g., `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#ASPECT_RATIO_SQUARE_1_1:kotlin.Int`).

If the aspect ratio is not set by the caller app using `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams.Builder#setAspectRatio(kotlin.Int)`, this method returns `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#ASPECT_RATIO_UNDEFINED:kotlin.Int`, indicating that the photo picker will use its default 1:1 media grid aspect ratio.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#ASPECT_RATIO_UNDEFINED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#ASPECT_RATIO_SQUARE_1_1:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/photopicker/PhotoPickerUiCustomizationParams#ASPECT_RATIO_PORTRAIT_9_16:kotlin.Int` |

### writeToParcel

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<PhotoPickerUiCustomizationParams!>
```
