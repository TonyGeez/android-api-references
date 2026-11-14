Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# EmbeddedPhotoPickerFeatureInfo

```
class EmbeddedPhotoPickerFeatureInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.photopicker.EmbeddedPhotoPickerFeatureInfo](EmbeddedPhotoPickerFeatureInfo.md) |

An immutable parcel to carry information regarding desired features of caller for a given session.

Below features are currently supported in embedded photopicker.

- Mime type to filter media
- Accent color to change color of primary picker element
- Ordered selection of media items
- Max selection media count restriction
- Pre-selected uris
- Theme night mode
- Highlighting media results based on a given input query including highlighting media results from certain albums
- Location metadata request
- Selection options for media items
- UI customization options for the embedded photo picker

Callers should use `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo.Builder` to set the desired features.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo.Builder` <br /> |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_ALBUMS:kotlin.Int` Constant to indicate the Albums tab as the launch tab. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_IMAGES:kotlin.Int` Constant to indicate the Photos tab as the launch tab. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_UNSET:kotlin.Int` Constant to indicate default tab when no tab has been set as the launch tab. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAccentColor <br /> |
| [EmbeddedPhotoPickerUiCustomizationParams](EmbeddedPhotoPickerUiCustomizationParams.md)? | getEmbeddedUiCustomizationParams Returns the embedded-specific UI customization options set by the app. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getHighlightAlbumId Returns the highlight album set by the app |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getHighlightSearchMediaTextQuery Returns the highlight media text query set by the app |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getHighlightType Returns the highlight type set by the app |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getLaunchTab Returns the launch tab set by the app. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getMaxSelectionLimit <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | getMimeTypes <br /> |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\> | getPreSelectedUris <br /> |
| [PhotoPickerSelectionParams](../android/widget/photopicker/PhotoPickerSelectionParams.md)? | getSelectionParams Returns the selection options, which specify filters for media item properties. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getThemeNightMode <br /> |
| --- | --- |
| [PhotoPickerUiCustomizationParams](PhotoPickerUiCustomizationParams.md)? | getUiCustomizationParams Returns the ui customization options set by the app. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isCollapsedModeScrollingEnabled Returns whether the app enabled scrolling in collapsed mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isLocationMetadataRequested Returns whether the app is requesting location metadata for selected media items. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isOrderedSelection <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isPickerLaunchedInExpandedState Returns whether or not the picker was launched in expanded state |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [EmbeddedPhotoPickerFeatureInfo](EmbeddedPhotoPickerFeatureInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### TAB_ALBUMS

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
static val TAB_ALBUMS: Int
```

Constant to indicate the Albums tab as the launch tab.

 Value: 0

### TAB_IMAGES

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
static val TAB_IMAGES: Int
```

Constant to indicate the Photos tab as the launch tab.

 Value: 1

### TAB_UNSET

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
static val TAB_UNSET: Int
```

Constant to indicate default tab when no tab has been set as the launch tab.

 Value: -1

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAccentColor

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun getAccentColor(): Long
```

### getEmbeddedUiCustomizationParams

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getEmbeddedUiCustomizationParams(): EmbeddedPhotoPickerUiCustomizationParams?
```

Returns the embedded-specific UI customization options set by the app.

| Return ||
|---|---|
| EmbeddedPhotoPickerUiCustomizationParams | The EmbeddedPhotoPickerUiCustomizationParams object, or `null` if no custom embedded options are set. |

### getHighlightAlbumId

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
fun getHighlightAlbumId(): String
```

Returns the highlight album set by the app

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getHighlightSearchMediaTextQuery

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 19](https://developer.android.com/sdkExtensions)

```
fun getHighlightSearchMediaTextQuery(): String
```

Returns the highlight media text query set by the app

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getHighlightType

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
fun getHighlightType(): Int
```

Returns the highlight type set by the app

### getLaunchTab

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getLaunchTab(): Int
```

Returns the launch tab set by the app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The launch tab for the embedded PhotoPicker, which is one of the android.widget.photopicker.EmbeddedPhotoPickerFeatureInfo.LaunchTab values (e.g., `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_IMAGES:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_ALBUMS:kotlin.Int`). If no launch tab is set then `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_UNSET:kotlin.Int` is the default value. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_UNSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_ALBUMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo#TAB_IMAGES:kotlin.Int` |

### getMaxSelectionLimit

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun getMaxSelectionLimit(): Int
```

### getMimeTypes

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun getMimeTypes(): MutableList<String!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getPreSelectedUris

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun getPreSelectedUris(): MutableList<Uri!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>` | This value cannot be `null`. |

### getSelectionParams

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions)

```
fun getSelectionParams(): PhotoPickerSelectionParams?
```

Returns the selection options, which specify filters for media item properties.

| Return ||
|---|---|
| PhotoPickerSelectionParams | The PhotoPickerSelectionParams object containing the selection filters, or `null` if no custom selection options are set. |

### getThemeNightMode

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun getThemeNightMode(): Int
```

### getUiCustomizationParams

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 22](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUiCustomizationParams(): PhotoPickerUiCustomizationParams?
```

**Deprecated:** *Use getEmbeddedUiCustomizationParams instead.*

Returns the ui customization options set by the app.

| Return ||
|---|---|
| PhotoPickerUiCustomizationParams | The PhotoPickerUiCustomizationParams object containing the ui customization options, or `null` if no custom options are set. |

### isCollapsedModeScrollingEnabled

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
fun isCollapsedModeScrollingEnabled(): Boolean
```

Returns whether the app enabled scrolling in collapsed mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the app enabled scrolling in collapsed mode, `false` otherwise. |

### isLocationMetadataRequested

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 23](https://developer.android.com/sdkExtensions)

```
fun isLocationMetadataRequested(): Boolean
```

Returns whether the app is requesting location metadata for selected media items.

### isOrderedSelection

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
fun isOrderedSelection(): Boolean
```

### isPickerLaunchedInExpandedState

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 21](https://developer.android.com/sdkExtensions)

```
fun isPickerLaunchedInExpandedState(): Boolean
```

Returns whether or not the picker was launched in expanded state

### toString

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<EmbeddedPhotoPickerFeatureInfo!>
```
