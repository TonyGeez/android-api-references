# WallpaperInfo

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WallpaperInfo

Kotlin| [Java](WallpaperInfo.md) 
| --- | --- |

```
class WallpaperInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.WallpaperInfo](WallpaperInfo.md) |

This class is used to specify meta information of a wallpaper service.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WallpaperInfo](WallpaperInfo.md))`(`context:` ` [Context](../android.content/Context.md)!`, `service:` ` [ResolveInfo](../android.content.pm/ResolveInfo.md)!`)` Constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](WallpaperInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](WallpaperInfo.md))`(`pw:` ` [Printer](../android.util/Printer.md)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [ComponentName](../android.content/ComponentName.md)! | [getComponent](WallpaperInfo.md))`()` Return the component of the service that implements this wallpaper. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPackageName](WallpaperInfo.md))`()` Return the . |
| [ServiceInfo](../android.content.pm/ServiceInfo.md)! | [getServiceInfo](WallpaperInfo.md))`()` Return the raw information about the Service implementing this wallpaper. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceName](WallpaperInfo.md))`()` Return the class name of the service component that implements this wallpaper. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSettingsActivity](WallpaperInfo.md))`()` Return the class name of an activity that provides a settings UI for the wallpaper. |
| [Uri](../android.net/Uri.md)? | [getSettingsSliceUri](WallpaperInfo.md))`()` Returns an URI that provides a settings [Slice](../android.app.slice/Slice.md) for this wallpaper. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShowMetadataInPreview](WallpaperInfo.md))`()` Queries whether any metadata should be shown when previewing the wallpaper. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadAuthor](WallpaperInfo.md))`(`pm:` ` [PackageManager](../android.content.pm/PackageManager.md)!`)` Return a string indicating the author(s) of this wallpaper. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadContextDescription](WallpaperInfo.md))`(`pm:` ` [PackageManager](../android.content.pm/PackageManager.md)!`)` Retrieves a title of the URI that specifies a link for further context about this wallpaper. |
| [Uri](../android.net/Uri.md)! | [loadContextUri](WallpaperInfo.md))`(`pm:` ` [PackageManager](../android.content.pm/PackageManager.md)!`)` Returns an URI that specifies a link for further context about this wallpaper. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadDescription](WallpaperInfo.md))`(`pm:` ` [PackageManager](../android.content.pm/PackageManager.md)!`)` Return a brief summary of this wallpaper's behavior. |
| [Drawable](../android.graphics.drawable/Drawable.md)! | [loadIcon](WallpaperInfo.md))`(`pm:` ` [PackageManager](../android.content.pm/PackageManager.md)!`)` Load the user-displayed icon for this wallpaper. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadLabel](WallpaperInfo.md))`(`pm:` ` [PackageManager](../android.content.pm/PackageManager.md)!`)` Load the user-displayed label for this wallpaper. |
| --- | --- |
| [Drawable](../android.graphics.drawable/Drawable.md)! | [loadThumbnail](WallpaperInfo.md))`(`pm:` ` [PackageManager](../android.content.pm/PackageManager.md)!`)` Load the thumbnail image for this wallpaper. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldUseDefaultUnfoldTransition](WallpaperInfo.md))`()` Returns whether this wallpaper should receive default zooming updates when the device changes its state (e.g. when folding or unfolding a foldable device). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMultipleDisplays](WallpaperInfo.md))`()` Returns whether this wallpaper service can support multiple engines to render on each surface independently. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](WallpaperInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](WallpaperInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android.os/Parcel.md). |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [WallpaperInfo](WallpaperInfo.md)!\> | [CREATOR](WallpaperInfo.md) Used to make this class parcelable. |

## Public constructors

### WallpaperInfo

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WallpaperInfo(
    context: Context!, 
    service: ResolveInfo!)
```

Constructor.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The Context in which we are parsing the wallpaper. |
| `service` | [ResolveInfo](../android.content.pm/ResolveInfo.md)!:The ResolveInfo returned from the package manager about this wallpaper's component. |

## Public methods

### describeContents

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### dump

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```  

### getComponent

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getComponent(): ComponentName!
```

Return the component of the service that implements this wallpaper. 

### getPackageName

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String!
```

Return the .apk package that implements this wallpaper. 

### getServiceInfo

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceInfo(): ServiceInfo!
```

Return the raw information about the Service implementing this wallpaper. Do not modify the returned object. 

### getServiceName

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceName(): String!
```

Return the class name of the service component that implements this wallpaper. 

### getSettingsActivity

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSettingsActivity(): String!
```

Return the class name of an activity that provides a settings UI for the wallpaper. You can launch this activity be starting it with an [android.content.Intent](../android.content/Intent.md) whose action is MAIN and with an explicit [android.content.ComponentName](../android.content/ComponentName.md) composed of [getPackageName](WallpaperInfo.md))and the class name returned here.

`null`will be returned if there is no settings activity associated with the wallpaper. 

### getSettingsSliceUri

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSettingsSliceUri(): Uri?
```

Returns an URI that provides a settings [Slice](../android.app.slice/Slice.md) for this wallpaper. The wallpaper should implement a SliceProvider associated with this URI. The system will display the Slice in the customization section while previewing the live wallpaper. Because this URI is accessible to other apps, it is recommended to protect it with the android.permission.BIND_WALLPAPER permission.

`null`will be returned if there is no settings Slice URI associated with the wallpaper.

| Return ||
|------------------------------------------------------------------------------|----------|
| [Uri](../android.net/Uri.md)? | The URI. |

### getShowMetadataInPreview

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getShowMetadataInPreview(): Boolean
```

Queries whether any metadata should be shown when previewing the wallpaper. If this value is set to true, any component that shows a preview of this live wallpaper should also show accompanying information like [loadLabel](WallpaperInfo.md)), [loadDescription](WallpaperInfo.md)), [loadAuthor](WallpaperInfo.md))and [loadContextDescription(android.content.pm.PackageManager)](WallpaperInfo.md)), so the user gets to know further information about this wallpaper.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether any metadata should be shown when previewing the wallpaper. |

### loadAuthor

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadAuthor(pm: PackageManager!): CharSequence!
```

Return a string indicating the author(s) of this wallpaper. 

### loadContextDescription

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadContextDescription(pm: PackageManager!): CharSequence!
```

Retrieves a title of the URI that specifies a link for further context about this wallpaper.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!:An instance of [PackageManager](../android.content.pm/PackageManager.md) to retrieve the title. |

| Return ||
|------------------------------------------------------------------------------------------------|------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The title. |

### loadContextUri

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadContextUri(pm: PackageManager!): Uri!
```

Returns an URI that specifies a link for further context about this wallpaper.

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!:An instance of [PackageManager](../android.content.pm/PackageManager.md) to retrieve the URI. |

| Return ||
|------------------------------------------------------------------------------|----------|
| [Uri](../android.net/Uri.md)! | The URI. |

### loadDescription

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadDescription(pm: PackageManager!): CharSequence!
```

Return a brief summary of this wallpaper's behavior. 

### loadIcon

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadIcon(pm: PackageManager!): Drawable!
```

Load the user-displayed icon for this wallpaper.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!:Supply a PackageManager used to load the wallpaper's resources. |

### loadLabel

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadLabel(pm: PackageManager!): CharSequence!
```

Load the user-displayed label for this wallpaper.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!:Supply a PackageManager used to load the wallpaper's resources. |

### loadThumbnail

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadThumbnail(pm: PackageManager!): Drawable!
```

Load the thumbnail image for this wallpaper.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](../android.content.pm/PackageManager.md)!:Supply a PackageManager used to load the wallpaper's resources. |

### shouldUseDefaultUnfoldTransition

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shouldUseDefaultUnfoldTransition(): Boolean
```

Returns whether this wallpaper should receive default zooming updates when the device changes its state (e.g. when folding or unfolding a foldable device). If set to false the wallpaper will not receive zoom events when changing the device state, so it can implement its own transition instead.

This corresponds to the value [android.R.styleable#Wallpaper_shouldUseDefaultUnfoldTransition](../android/R.styleable.md) in the XML description of the wallpaper.

The default value is`true`.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if wallpaper should receive default device state change transition updates |

**See Also**

- [android.R.styleable#Wallpaper_shouldUseDefaultUnfoldTransition](../android/R.styleable.md) 

### supportsMultipleDisplays

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun supportsMultipleDisplays(): Boolean
```

Returns whether this wallpaper service can support multiple engines to render on each surface independently. An example use case is a multi-display set-up where the wallpaper service can render surfaces to each of the connected displays.

This corresponds to the value [android.R.styleable#Wallpaper_supportsMultipleDisplays](../android/R.styleable.md) in the XML description of the wallpaper.

The default value is`false`.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if multiple engines can render independently on each surface. |

**See Also**

- [android.service.wallpaper.WallpaperService#onCreateEngine()](../android.service.wallpaper/WallpaperService.md))
- [android.service.wallpaper.WallpaperService.Engine#onCreate(SurfaceHolder)](../android/service/wallpaper/WallpaperService.Engine.md)) 

### toString

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](../android.os/Parcel.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The [Parcel](../android.os/Parcel.md) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WallpaperInfo!>
```

Used to make this class parcelable.
