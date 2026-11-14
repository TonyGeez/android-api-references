# WallpaperInfo

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WallpaperInfo

Kotlin| [Java](https://developer.android.com/reference/android/app/WallpaperInfo "View this page in Java") 
| --- | --- |

```
class WallpaperInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.WallpaperInfo](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#) |

This class is used to specify meta information of a wallpaper service.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WallpaperInfo](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#WallpaperInfo(android.content.Context,%20android.content.pm.ResolveInfo))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `service:` ` [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!`)` Constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#describeContents())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#dump(android.util.Printer,%20kotlin.String))`(`pw:` ` [Printer](https://developer.android.com/reference/kotlin/android/util/Printer.html#)!`, `prefix:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)! | [getComponent](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#getComponent())`()` Return the component of the service that implements this wallpaper. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPackageName](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#getPackageName())`()` Return the . |
| [ServiceInfo](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#)! | [getServiceInfo](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#getServiceInfo())`()` Return the raw information about the Service implementing this wallpaper. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceName](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#getServiceName())`()` Return the class name of the service component that implements this wallpaper. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSettingsActivity](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#getSettingsActivity())`()` Return the class name of an activity that provides a settings UI for the wallpaper. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getSettingsSliceUri](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#getSettingsSliceUri())`()` Returns an URI that provides a settings [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice) for this wallpaper. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShowMetadataInPreview](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#getShowMetadataInPreview())`()` Queries whether any metadata should be shown when previewing the wallpaper. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadAuthor](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadAuthor(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Return a string indicating the author(s) of this wallpaper. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadContextDescription](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadContextDescription(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Retrieves a title of the URI that specifies a link for further context about this wallpaper. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [loadContextUri](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadContextUri(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Returns an URI that specifies a link for further context about this wallpaper. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadDescription](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadDescription(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Return a brief summary of this wallpaper's behavior. |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | [loadIcon](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadIcon(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Load the user-displayed icon for this wallpaper. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [loadLabel](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadLabel(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Load the user-displayed label for this wallpaper. |
| --- | --- |
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | [loadThumbnail](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadThumbnail(android.content.pm.PackageManager))`(`pm:` ` [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!`)` Load the thumbnail image for this wallpaper. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldUseDefaultUnfoldTransition](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#shouldUseDefaultUnfoldTransition())`()` Returns whether this wallpaper should receive default zooming updates when the device changes its state (e.g. when folding or unfolding a foldable device). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [supportsMultipleDisplays](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#supportsMultipleDisplays())`()` Returns whether this wallpaper service can support multiple engines to render on each surface independently. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [WallpaperInfo](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#CREATOR:android.os.Parcelable.Creator) Used to make this class parcelable. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The Context in which we are parsing the wallpaper. |
| `service` | [ResolveInfo](https://developer.android.com/reference/kotlin/android/content/pm/ResolveInfo.html#)!:The ResolveInfo returned from the package manager about this wallpaper's component. |

## Public methods

### describeContents

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Return the class name of an activity that provides a settings UI for the wallpaper. You can launch this activity be starting it with an [android.content.Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) whose action is MAIN and with an explicit [android.content.ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#) composed of [getPackageName](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#getPackageName())and the class name returned here.

`null`will be returned if there is no settings activity associated with the wallpaper. 

### getSettingsSliceUri

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSettingsSliceUri(): Uri?
```

Returns an URI that provides a settings [Slice](https://developer.android.com/reference/kotlin/android/app/slice/Slice) for this wallpaper. The wallpaper should implement a SliceProvider associated with this URI. The system will display the Slice in the customization section while previewing the live wallpaper. Because this URI is accessible to other apps, it is recommended to protect it with the android.permission.BIND_WALLPAPER permission.

`null`will be returned if there is no settings Slice URI associated with the wallpaper.

| Return ||
|------------------------------------------------------------------------------|----------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | The URI. |

### getShowMetadataInPreview

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getShowMetadataInPreview(): Boolean
```

Queries whether any metadata should be shown when previewing the wallpaper. If this value is set to true, any component that shows a preview of this live wallpaper should also show accompanying information like [loadLabel](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadLabel(android.content.pm.PackageManager)), [loadDescription](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadDescription(android.content.pm.PackageManager)), [loadAuthor](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadAuthor(android.content.pm.PackageManager))and [loadContextDescription(android.content.pm.PackageManager)](https://developer.android.com/reference/kotlin/android/app/WallpaperInfo#loadContextDescription(android.content.pm.PackageManager)), so the user gets to know further information about this wallpaper.

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
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!:An instance of [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#) to retrieve the title. |

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
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!:An instance of [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#) to retrieve the URI. |

| Return ||
|------------------------------------------------------------------------------|----------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | The URI. |

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
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!:Supply a PackageManager used to load the wallpaper's resources. |

### loadLabel

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadLabel(pm: PackageManager!): CharSequence!
```

Load the user-displayed label for this wallpaper.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!:Supply a PackageManager used to load the wallpaper's resources. |

### loadThumbnail

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun loadThumbnail(pm: PackageManager!): Drawable!
```

Load the thumbnail image for this wallpaper.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pm` | [PackageManager](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#)!:Supply a PackageManager used to load the wallpaper's resources. |

### shouldUseDefaultUnfoldTransition

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun shouldUseDefaultUnfoldTransition(): Boolean
```

Returns whether this wallpaper should receive default zooming updates when the device changes its state (e.g. when folding or unfolding a foldable device). If set to false the wallpaper will not receive zoom events when changing the device state, so it can implement its own transition instead.

This corresponds to the value [android.R.styleable#Wallpaper_shouldUseDefaultUnfoldTransition](https://developer.android.com/reference/kotlin/android/R.styleable.html#Wallpaper_shouldUseDefaultUnfoldTransition:kotlin.Int) in the XML description of the wallpaper.

The default value is`true`.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if wallpaper should receive default device state change transition updates |

**See Also**

- [android.R.styleable#Wallpaper_shouldUseDefaultUnfoldTransition](https://developer.android.com/reference/kotlin/android/R.styleable.html#Wallpaper_shouldUseDefaultUnfoldTransition:kotlin.Int) 

### supportsMultipleDisplays

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun supportsMultipleDisplays(): Boolean
```

Returns whether this wallpaper service can support multiple engines to render on each surface independently. An example use case is a multi-display set-up where the wallpaper service can render surfaces to each of the connected displays.

This corresponds to the value [android.R.styleable#Wallpaper_supportsMultipleDisplays](https://developer.android.com/reference/kotlin/android/R.styleable.html#Wallpaper_supportsMultipleDisplays:kotlin.Int) in the XML description of the wallpaper.

The default value is`false`.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if multiple engines can render independently on each surface. |

**See Also**

- [android.service.wallpaper.WallpaperService#onCreateEngine()](https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.html#onCreateEngine())
- [android.service.wallpaper.WallpaperService.Engine#onCreate(SurfaceHolder)](https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.Engine.html#onCreate(android.view.SurfaceHolder)) 

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

Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<WallpaperInfo!>
```

Used to make this class parcelable.
