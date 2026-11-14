Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WallpaperManager

Kotlin | [Java](WallpaperManager.md)
| --- | --- |

```
open class WallpaperManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.WallpaperManager](WallpaperManager.md) |

Provides access to the system wallpaper. With WallpaperManager, you can get the current wallpaper, get the desired dimensions for the wallpaper, set the wallpaper, and more.

An app can check whether wallpapers are supported for the current user, by calling `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#isWallpaperSupported()`, and whether setting of wallpapers is allowed, by calling `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#isSetWallpaperAllowed()`. Any public APIs added to WallpaperManager should have a corresponding stub in `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager.OnColorsChangedListener` Interface definition for a callback to be invoked when colors change on a wallpaper. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#ACTION_CHANGE_LIVE_WALLPAPER:kotlin.String` Directly launch live wallpaper preview, allowing the user to immediately confirm to switch to a specific live wallpaper. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#ACTION_CROP_AND_SET_WALLPAPER:kotlin.String` Activity Action: Show settings for choosing wallpaper. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#ACTION_LIVE_WALLPAPER_CHOOSER:kotlin.String` Launch an activity for the user to pick the current global live wallpaper. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#COMMAND_DROP:kotlin.String` Command for `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#sendWallpaperCommand(android.os.IBinder,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)`: reported by the wallpaper host when the user drops an object into an area of the host. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#COMMAND_SECONDARY_TAP:kotlin.String` Command for `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#sendWallpaperCommand(android.os.IBinder,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)`: reported by the wallpaper host when the user releases a secondary pointer on an empty area (not performing an action in the host). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#COMMAND_TAP:kotlin.String` Command for `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#sendWallpaperCommand(android.os.IBinder,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)`: reported by the wallpaper host when the user taps on an empty area (not performing an action in the host). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#EXTRA_LIVE_WALLPAPER_COMPONENT:kotlin.String` Extra in `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#ACTION_CHANGE_LIVE_WALLPAPER:kotlin.String` that specifies the ComponentName of a live wallpaper that should be shown as a preview, for the user to confirm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` Flag: set or retrieve the lock-screen-specific wallpaper. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` Flag: set or retrieve the general system wallpaper. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#WALLPAPER_PREVIEW_META_DATA:kotlin.String` Manifest entry for activities that respond to `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SET_WALLPAPER:kotlin.String` which allows them to provide a custom large icon associated with this action. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#addOnColorsChangedListener(android.app.WallpaperManager.OnColorsChangedListener,%20android.os.Handler)(listener: https://developer.android.com/reference/kotlin/android/app/WallpaperManager.OnColorsChangedListener, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#)` Registers a listener to get notified when the wallpaper colors change. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#clear()()` Remove any currently set system wallpaper, reverting to the system's built-in wallpaper. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#clear(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove one or more currently set wallpapers, reverting to the system default display for each one. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#clearWallpaper()()` Equivalent to `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#clear()`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#clearWallpaperOffsets(android.os.IBinder)(windowToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!)` Clear the offsets previously associated with this window through `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setWallpaperOffsets(android.os.IBinder,%20kotlin.Float,%20kotlin.Float)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#forgetLoadedWallpaper()()` Remove all internal references to the last loaded wallpaper. |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getBuiltInDrawable()()` Obtain a drawable for the built-in static system wallpaper. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getBuiltInDrawable(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Obtain a drawable for the specified built-in static system wallpaper. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getBuiltInDrawable(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float,%20kotlin.Float)(outWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, outHeight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scaleToFit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, horizontalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns a drawable for the system built-in static wallpaper. |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getBuiltInDrawable(kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Float,%20kotlin.Float,%20kotlin.Int)(outWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, outHeight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, scaleToFit: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, horizontalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a drawable for the built-in static wallpaper of the specified type. |
| open [Intent](../android.content/Intent.md)! | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getCropAndSetWallpaperIntent(android.net.Uri)(imageUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Gets an Intent that will launch an activity that crops the given image and sets the device's wallpaper. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDesiredMinimumHeight()()` Returns the desired minimum height for the wallpaper. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDesiredMinimumWidth()()` Returns the desired minimum width for the wallpaper. |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable()()` **Important note:** - Up to Android 12, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission. - Starting in Android 13, directly accessing the wallpaper is not possible anymore, instead the default system wallpaper is returned (some versions of Android 13 may throw a `SecurityException`). - From Android 14, this method should not be used and will always throw a `SecurityException`. - Apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` can still access the real wallpaper on all versions. <br /> |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Important note:** only apps with should use this method. |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getFastDrawable()()` **Important note:** - Up to Android 12, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission. - Starting in Android 13, directly accessing the wallpaper is not possible anymore, instead the default wallpaper is returned (some versions of Android 13 may throw a `SecurityException`). - From Android 14, this method should not be used and will always throw a `SecurityException`. - Apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` can still access the real wallpaper on all versions. <br /> |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getFastDrawable(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Important note:** only apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` should use this method. |
| open static [WallpaperManager](WallpaperManager.md)! | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getInstance(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Retrieve a WallpaperManager associated with the given Context. |
| --- | --- |
| open [WallpaperColors](WallpaperColors.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getWallpaperColors(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the primary colors of a wallpaper. |
| open [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getWallpaperFile(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Important note:** - Up to Android 12, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission. - Starting in Android 13, directly accessing the wallpaper is not possible anymore, instead the default system wallpaper is returned (some versions of Android 13 may throw a `SecurityException`). - From Android 14, this method should not be used and will always throw a `SecurityException`. - Apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` can still access the real wallpaper on all versions. <br /> Get an open, readable file descriptor to the given wallpaper image file. <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getWallpaperId(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the ID of the current wallpaper of the given kind. |
| --- | --- |
| open [WallpaperInfo](WallpaperInfo.md)! | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getWallpaperInfo()()` Returns the information about the home screen wallpaper if its current wallpaper is a live wallpaper component. |
| open [WallpaperInfo](WallpaperInfo.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getWallpaperInfo(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the information about the designated wallpaper if its current wallpaper is a live wallpaper component. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#hasResourceWallpaper(kotlin.Int)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return whether any users are currently set to use the wallpaper with the given resource ID. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#isSetWallpaperAllowed()()` Returns whether the calling package is allowed to set the wallpaper for the calling user. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#isWallpaperSupported()()` Returns whether wallpapers are supported for the calling user. |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#peekDrawable()()` **Important note:** - Up to Android 12, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission. - Starting in Android 13, directly accessing the wallpaper is not possible anymore, instead the default system wallpaper is returned (some versions of Android 13 may throw a `SecurityException`). - From Android 14, this method should not be used and will always throw a `SecurityException`. - Apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` can still access the real wallpaper on all versions. <br /> |
| --- | --- |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#peekDrawable(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Important note:** only apps with should use this method. |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#peekFastDrawable()()` **Important note:** only apps with should use this method. |
| open [Drawable](../android.graphics.drawable/Drawable.md)? | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#peekFastDrawable(kotlin.Int)(which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` **Important note:** only apps with should use this method. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#removeOnColorsChangedListener(android.app.WallpaperManager.OnColorsChangedListener)(callback: https://developer.android.com/reference/kotlin/android/app/WallpaperManager.OnColorsChangedListener)` Stop listening to color updates. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#sendWallpaperCommand(android.os.IBinder,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)(windowToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, action: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, z: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Send an arbitrary command to the current active wallpaper. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setBitmap(android.graphics.Bitmap)(bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!)` Change the current system wallpaper to a bitmap. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setBitmap(android.graphics.Bitmap,%20android.graphics.Rect,%20kotlin.Boolean)(fullImage: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!, visibleCropHint: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, allowBackup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Change the current system wallpaper to a bitmap, specifying a hint about which subrectangle of the full image is to be visible. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setBitmap(android.graphics.Bitmap,%20android.graphics.Rect,%20kotlin.Boolean,%20kotlin.Int)(fullImage: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#!, visibleCropHint: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, allowBackup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Version of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setBitmap(android.graphics.Bitmap,%20android.graphics.Rect,%20kotlin.Boolean)` that allows the caller to specify which of the supported wallpaper categories to set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setDisplayPadding(android.graphics.Rect)(padding: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!)` Specify extra padding that the wallpaper should have outside of the display. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setResource(kotlin.Int)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Change the current system wallpaper to the bitmap in the given resource. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setResource(kotlin.Int,%20kotlin.Int)(resid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Version of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setResource(kotlin.Int)` that allows the caller to specify which of the supported wallpaper categories to set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setStream(java.io.InputStream)(bitmapData: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` Change the current system wallpaper to a specific byte stream. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setStream(java.io.InputStream,%20android.graphics.Rect,%20kotlin.Boolean)(bitmapData: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!, visibleCropHint: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, allowBackup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Change the current system wallpaper to a specific byte stream, specifying a hint about which subrectangle of the full image is to be visible. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setStream(java.io.InputStream,%20android.graphics.Rect,%20kotlin.Boolean,%20kotlin.Int)(bitmapData: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!, visibleCropHint: https://developer.android.com/reference/kotlin/android/graphics/Rect.html#!, allowBackup: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Version of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setStream(java.io.InputStream,%20android.graphics.Rect,%20kotlin.Boolean)` that allows the caller to specify which of the supported wallpaper categories to set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setWallpaperOffsetSteps(kotlin.Float,%20kotlin.Float)(xStep: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, yStep: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` For applications that use multiple virtual screens showing a wallpaper, specify the step size between virtual screens. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setWallpaperOffsets(android.os.IBinder,%20kotlin.Float,%20kotlin.Float)(windowToken: https://developer.android.com/reference/kotlin/android/os/IBinder.html#!, xOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, yOffset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set the display position of the current wallpaper within any larger space, when that wallpaper is visible behind the given window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#suggestDesiredDimensions(kotlin.Int,%20kotlin.Int)(minimumWidth: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, minimumHeight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` For use only by the current home application, to specify the size of wallpaper it would like to use. |

## Constants

### ACTION_CHANGE_LIVE_WALLPAPER

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CHANGE_LIVE_WALLPAPER: String
```

Directly launch live wallpaper preview, allowing the user to immediately confirm to switch to a specific live wallpaper. You must specify `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#EXTRA_LIVE_WALLPAPER_COMPONENT:kotlin.String` with the ComponentName of a live wallpaper component that is to be shown.

 Value: "android.service.wallpaper.CHANGE_LIVE_WALLPAPER"

### ACTION_CROP_AND_SET_WALLPAPER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CROP_AND_SET_WALLPAPER: String
```

Activity Action: Show settings for choosing wallpaper. Do not use directly to construct an intent; instead, use `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getCropAndSetWallpaperIntent(android.net.Uri)`.

Input: `https://developer.android.com/reference/kotlin/android/content/Intent.html#getData()` is the URI of the image to crop and set as wallpaper.

Output: RESULT_OK if user decided to crop/set the wallpaper, RESULT_CANCEL otherwise Activities that support this intent should specify a MIME filter of "image/\*"

 Value: "android.service.wallpaper.CROP_AND_SET_WALLPAPER"

### ACTION_LIVE_WALLPAPER_CHOOSER

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LIVE_WALLPAPER_CHOOSER: String
```

Launch an activity for the user to pick the current global live wallpaper.

 Value: "android.service.wallpaper.LIVE_WALLPAPER_CHOOSER"

### COMMAND_DROP

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMMAND_DROP: String
```

Command for `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#sendWallpaperCommand(android.os.IBinder,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)`: reported by the wallpaper host when the user drops an object into an area of the host. The x and y arguments are the location of the drop.

 Value: "android.home.drop"

### COMMAND_SECONDARY_TAP

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMMAND_SECONDARY_TAP: String
```

Command for `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#sendWallpaperCommand(android.os.IBinder,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)`: reported by the wallpaper host when the user releases a secondary pointer on an empty area (not performing an action in the host). The x and y arguments are the location of the secondary tap in screen coordinates.

 Value: "android.wallpaper.secondaryTap"

### COMMAND_TAP

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COMMAND_TAP: String
```

Command for `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#sendWallpaperCommand(android.os.IBinder,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle)`: reported by the wallpaper host when the user taps on an empty area (not performing an action in the host). The x and y arguments are the location of the tap in screen coordinates.

 Value: "android.wallpaper.tap"

### EXTRA_LIVE_WALLPAPER_COMPONENT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LIVE_WALLPAPER_COMPONENT: String
```

Extra in `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#ACTION_CHANGE_LIVE_WALLPAPER:kotlin.String` that specifies the ComponentName of a live wallpaper that should be shown as a preview, for the user to confirm.

 Value: "android.service.wallpaper.extra.LIVE_WALLPAPER_COMPONENT"

### FLAG_LOCK

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_LOCK: Int
```

Flag: set or retrieve the lock-screen-specific wallpaper.

 Value: 2

### FLAG_SYSTEM

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SYSTEM: Int
```

Flag: set or retrieve the general system wallpaper.

 Value: 1

### WALLPAPER_PREVIEW_META_DATA

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val WALLPAPER_PREVIEW_META_DATA: String
```

Manifest entry for activities that respond to `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_SET_WALLPAPER:kotlin.String` which allows them to provide a custom large icon associated with this action.

 Value: "android.wallpaper.preview"

## Public methods

### addOnColorsChangedListener

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addOnColorsChangedListener(
    listener: WallpaperManager.OnColorsChangedListener, 
    handler: Handler
): Unit
```

Registers a listener to get notified when the wallpaper colors change.

| Parameters ||
|---|---|
| `listener` | [WallpaperManager.OnColorsChangedListener](../android/app/WallpaperManager.OnColorsChangedListener.md): A listener to register. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md): Where to call it from. Will be called from the main thread if null. |

### clear

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Remove any currently set system wallpaper, reverting to the system's built-in wallpaper. On success, the intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WALLPAPER_CHANGED:kotlin.String` is broadcast.

This method requires the caller to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Exceptions ||
|---|---|
| `java.io.IOException` | If an error occurs reverting to the built-in wallpaper. |

### clear

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(which: Int): Unit
```

Remove one or more currently set wallpapers, reverting to the system default display for each one. On success, the intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WALLPAPER_CHANGED:kotlin.String` is broadcast.

- When called with `which=``https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`, clear the lockscreen wallpaper. The home screen wallpaper will become visible on the lock screen.
- When called with `which=``https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`, revert the home screen wallpaper to default. The lockscreen wallpaper will be unchanged: if the previous wallpaper was shared between home and lock screen, it will become lock screen only.
- When called with `which=`(`https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` | `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`), put the default wallpaper on both home and lock screen, removing any user defined wallpaper.
| --- | --- |

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

<br />

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A bitwise combination of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an error occurs reverting to the built-in wallpaper. |

### clearWallpaper

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearWallpaper(): Unit
```

Equivalent to `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#clear()`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`
**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#clear()`

### clearWallpaperOffsets

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clearWallpaperOffsets(windowToken: IBinder!): Unit
```

Clear the offsets previously associated with this window through `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setWallpaperOffsets(android.os.IBinder,%20kotlin.Float,%20kotlin.Float)`. This reverts the window to its default state, where it does not cause the wallpaper to scroll from whatever its last offsets were.

| Parameters ||
|---|---|
| `windowToken` | [IBinder](../android.os/IBinder.md)!: The window who these offsets should be associated with, as returned by `https://developer.android.com/reference/kotlin/android/view/View.html#getWindowToken()`. |

### forgetLoadedWallpaper

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forgetLoadedWallpaper(): Unit
```

Remove all internal references to the last loaded wallpaper. Useful for apps that want to reduce memory usage when they only temporarily need to have the wallpaper. After calling, the next request for the wallpaper will require reloading it again from disk.

### getBuiltInDrawable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBuiltInDrawable(): Drawable!
```

Obtain a drawable for the built-in static system wallpaper.

### getBuiltInDrawable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBuiltInDrawable(which: Int): Drawable!
```

Obtain a drawable for the specified built-in static system wallpaper.

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `FLAG_*` identifier of a valid wallpaper type. Throws IllegalArgumentException if an invalid wallpaper is requested. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | A Drawable presenting the specified wallpaper image, or `null` if no built-in default image for that wallpaper type exists. |

### getBuiltInDrawable

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBuiltInDrawable(
    outWidth: Int, 
    outHeight: Int, 
    scaleToFit: Boolean, 
    horizontalAlignment: Float, 
    verticalAlignment: Float
): Drawable!
```

Returns a drawable for the system built-in static wallpaper. Based on the parameters, the drawable can be cropped and scaled

| Parameters ||
|---|---|
| `outWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the returned drawable |
| `scaleToFit` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, scale the wallpaper down rather than just cropping it |
| `horizontalAlignment` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A float value between 0 and 1 specifying where to crop the image; 0 for left-aligned, 0.5 for horizontal center-aligned, and 1 for right-aligned |
| --- | --- |
| `verticalAlignment` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A float value between 0 and 1 specifying where to crop the image; 0 for top-aligned, 0.5 for vertical center-aligned, and 1 for bottom-aligned |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | A Drawable presenting the built-in default system wallpaper image, or `null` if no such default image is defined on this device. |

### getBuiltInDrawable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBuiltInDrawable(
    outWidth: Int, 
    outHeight: Int, 
    scaleToFit: Boolean, 
    horizontalAlignment: Float, 
    verticalAlignment: Float, 
    which: Int
): Drawable!
```

Returns a drawable for the built-in static wallpaper of the specified type. Based on the parameters, the drawable can be cropped and scaled.

| Parameters ||
|---|---|
| `outWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the returned drawable |
| `scaleToFit` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): If true, scale the wallpaper down rather than just cropping it |
| `horizontalAlignment` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A float value between 0 and 1 specifying where to crop the image; 0 for left-aligned, 0.5 for horizontal center-aligned, and 1 for right-aligned |
| --- | --- |
| `verticalAlignment` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): A float value between 0 and 1 specifying where to crop the image; 0 for top-aligned, 0.5 for vertical center-aligned, and 1 for bottom-aligned |
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `FLAG_*` identifier of a valid wallpaper type. Throws IllegalArgumentException if an invalid wallpaper is requested. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | A Drawable presenting the built-in default wallpaper image of the given type, or `null` if no default image of that type is defined on this device. |

### getCropAndSetWallpaperIntent

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCropAndSetWallpaperIntent(imageUri: Uri!): Intent!
```

Gets an Intent that will launch an activity that crops the given image and sets the device's wallpaper. If there is a default HOME activity that supports cropping wallpapers, it will be preferred as the default. Use this method instead of directly creating a `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#ACTION_CROP_AND_SET_WALLPAPER:kotlin.String` intent.

| Parameters ||
|---|---|
| `imageUri` | [Uri](../android.net/Uri.md)!: The image URI that will be set in the intent. The must be a content URI and its provider must resolve its type to "image/\*" |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the URI is not a content URI or its MIME type is not "image/\*" |

### getDesiredMinimumHeight

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDesiredMinimumHeight(): Int
```

Returns the desired minimum height for the wallpaper. Callers of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setBitmap(android.graphics.Bitmap)` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setStream(java.io.InputStream)` should check this value beforehand to make sure the supplied wallpaper respects the desired minimum height. If the returned value is \<= 0, the caller should use the height of the default display instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The desired minimum height for the wallpaper. This value should be honored by applications that set the wallpaper but it is not mandatory. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDesiredMinimumWidth()`

### getDesiredMinimumWidth

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDesiredMinimumWidth(): Int
```

Returns the desired minimum width for the wallpaper. Callers of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setBitmap(android.graphics.Bitmap)` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setStream(java.io.InputStream)` should check this value beforehand to make sure the supplied wallpaper respects the desired minimum width. If the returned value is \<= 0, the caller should use the width of the default display instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The desired minimum width for the wallpaper. This value should be honored by applications that set the wallpaper but it is not mandatory. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDesiredMinimumHeight()`

### getDrawable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(): Drawable?
```

**Important note:**

- Up to Android 12, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission.
- Starting in Android 13, directly accessing the wallpaper is not possible anymore, instead the default system wallpaper is returned (some versions of Android 13 may throw a `SecurityException`).
- From Android 14, this method should not be used and will always throw a `SecurityException`.
- Apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` can still access the real wallpaper on all versions.

<br />

Equivalent to `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable(kotlin.Int)` with `which=``https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | A Drawable object for the requested wallpaper. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable(kotlin.Int)`

### getDrawable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(which: Int): Drawable?
```

**Important note:** only apps with should use this method. Otherwise, a `SecurityException` will be thrown.

Retrieve the requested wallpaper for the specified wallpaper type if the wallpaper is not a live wallpaper. This method should not be used to display the user wallpaper on an app: `https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_SHOW_WALLPAPER:kotlin.Int` should be used instead.

When called with `which=``https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`, if there is a live wallpaper on home screen, the built-in default wallpaper is returned.

When called with `which=``https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`, if there is a live wallpaper on lock screen, or if the lock screen and home screen share the same wallpaper engine, `null` is returned.

`https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getWallpaperInfo(kotlin.Int)` can be used to determine whether there is a live wallpaper on a specified screen type.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `FLAG_*` identifier of a valid wallpaper type. Throws IllegalArgumentException if an invalid wallpaper is requested. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | A Drawable object for the requested wallpaper. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

### getFastDrawable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFastDrawable(): Drawable?
```

**Important note:**

- Up to Android 12, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission.
- Starting in Android 13, directly accessing the wallpaper is not possible anymore, instead the default wallpaper is returned (some versions of Android 13 may throw a `SecurityException`).
- From Android 14, this method should not be used and will always throw a `SecurityException`.
- Apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` can still access the real wallpaper on all versions.

<br />

Equivalent to `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getFastDrawable(kotlin.Int)` with `which=``https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | A Drawable object for the requested wallpaper. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getFastDrawable(kotlin.Int)`

### getFastDrawable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFastDrawable(which: Int): Drawable?
```

**Important note:** only apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` should use this method. Otherwise, a `SecurityException` will be thrown. Like `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable(kotlin.Int)`, but the returned Drawable has a number of limitations to reduce its overhead as much as possible. It will never scale the wallpaper (only centering it if the requested bounds do match the bitmap bounds, which should not be typical), doesn't allow setting an alpha, color filter, or other attributes, etc. The bounds of the returned drawable will be initialized to the same bounds as the wallpaper, so normally you will not need to touch it. The drawable also assumes that it will be used in a context running in the same density as the screen (not in density compatibility mode). 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `FLAG_*` identifier of a valid wallpaper type. Throws IllegalArgumentException if an invalid wallpaper is requested. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | An optimized Drawable object for the requested wallpaper, or `null` in some cases as specified in `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable(kotlin.Int)`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

### getInstance

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(context: Context!): WallpaperManager!
```

Retrieve a WallpaperManager associated with the given Context.

### getWallpaperColors

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWallpaperColors(which: Int): WallpaperColors?
```

Get the primary colors of a wallpaper.

This method can return `null` when:

- Colors are still being processed by the system.
- The user has chosen to use a live wallpaper: live wallpapers might not implement `https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.Engine.html#onComputeColors()`.

Please note that this API will go through IPC and may take some time to calculate the wallpaper color, which could block the caller thread, so it is not recommended to call this in the UI thread.

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Wallpaper type. Must be either `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/WallpaperColors?` | Current `https://developer.android.com/reference/kotlin/android/app/WallpaperColors` or null if colors are unknown. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#addOnColorsChangedListener(android.app.WallpaperManager.OnColorsChangedListener,%20android.os.Handler)`

### getWallpaperFile

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWallpaperFile(which: Int): ParcelFileDescriptor?
```

**Important note:**

- Up to Android 12, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission.
- Starting in Android 13, directly accessing the wallpaper is not possible anymore, instead the default system wallpaper is returned (some versions of Android 13 may throw a `SecurityException`).
- From Android 14, this method should not be used and will always throw a `SecurityException`.
- Apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` can still access the real wallpaper on all versions.

<br />

Get an open, readable file descriptor to the given wallpaper image file. The caller is responsible for closing the file descriptor when done ingesting the file.

<br />

If no lock-specific wallpaper has been configured for the given user, then this method will return `null` when requesting `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` rather than returning the system wallpaper's image file. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The wallpaper whose image file is to be retrieved. Must be a single defined kind of wallpaper, either `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#?` | An open, readable file descriptor to the requested wallpaper image file; or `null` if no such wallpaper is configured or if the calling app does not have permission to read the current wallpaper. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`

### getWallpaperId

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWallpaperId(which: Int): Int
```

Get the ID of the current wallpaper of the given kind. If there is no such wallpaper configured, returns a negative number.

Every time the wallpaper image is set, a new ID is assigned to it. This method allows the caller to determine whether the wallpaper imagery has changed, regardless of how that change happened.

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The wallpaper whose ID is to be returned. Must be a single defined kind of wallpaper, either `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The positive numeric ID of the current wallpaper of the given kind, or a negative value if no such wallpaper is configured. |

### getWallpaperInfo

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWallpaperInfo(): WallpaperInfo!
```

Returns the information about the home screen wallpaper if its current wallpaper is a live wallpaper component. Otherwise, if the wallpaper is a static image or is not set, or if the caller doesn't have the appropriate permissions, this returns `null`.

For devices running Android 13 or earlier, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#QUERY_ALL_PACKAGES:kotlin.String` permission.

For devices running Android 14 or later, in order to use this, apps should declare a `<queries>` tag with the action `"android.service.wallpaper.WallpaperService"`. Otherwise, this method will return `null` if the caller doesn't otherwise have [visibility](https://developer.android.com/training/package-visibility) of the wallpaper package.

### getWallpaperInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWallpaperInfo(which: Int): WallpaperInfo?
```

Returns the information about the designated wallpaper if its current wallpaper is a live wallpaper component. Otherwise, if the wallpaper is a static image or is not set, or if the caller doesn't have the appropriate permissions, this returns `null`.

In order to use this, apps should declare a `<queries>` tag with the action `"android.service.wallpaper.WallpaperService"`. Otherwise, this method will return `null` if the caller doesn't otherwise have [visibility](https://developer.android.com/training/package-visibility) of the wallpaper package.

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Specifies wallpaper to request (home or lock). Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `which` is not exactly one of {`https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`,`https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`}. |

### hasResourceWallpaper

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasResourceWallpaper(resid: Int): Boolean
```

Return whether any users are currently set to use the wallpaper with the given resource ID. That is, their wallpaper has been set through `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setResource(kotlin.Int)` with the same resource id.

### isSetWallpaperAllowed

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSetWallpaperAllowed(): Boolean
```

Returns whether the calling package is allowed to set the wallpaper for the calling user. If this function returns `false`, any attempts to change the wallpaper will have no effect. Always returns `true` for device owner and profile owner.
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_SET_WALLPAPER:kotlin.String`

### isWallpaperSupported

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWallpaperSupported(): Boolean
```

Returns whether wallpapers are supported for the calling user. If this function returns `false`, any attempts to changing the wallpaper will have no effect, and any attempt to obtain of the wallpaper will return `null`.

### peekDrawable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekDrawable(): Drawable?
```

**Important note:**

- Up to Android 12, this method requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#READ_EXTERNAL_STORAGE:kotlin.String` permission.
- Starting in Android 13, directly accessing the wallpaper is not possible anymore, instead the default system wallpaper is returned (some versions of Android 13 may throw a `SecurityException`).
- From Android 14, this method should not be used and will always throw a `SecurityException`.
- Apps with `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` can still access the real wallpaper on all versions.

<br />

Equivalent to `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable()`.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | A Drawable object for the requested wallpaper. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable()`

### peekDrawable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekDrawable(which: Int): Drawable?
```

**Important note:** only apps with should use this method. Otherwise, a `SecurityException` will be thrown.

Equivalent to `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable(kotlin.Int)`.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `FLAG_*` identifier of a valid wallpaper type. Throws IllegalArgumentException if an invalid wallpaper is requested. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | A Drawable object for the requested wallpaper. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDrawable(kotlin.Int)`

### peekFastDrawable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekFastDrawable(): Drawable?
```

**Important note:** only apps with should use this method. Otherwise, a `SecurityException` will be thrown.

Equivalent to `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getFastDrawable()`.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | An optimized Drawable object for the requested wallpaper. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getFastDrawable()`

### peekFastDrawable

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekFastDrawable(which: Int): Drawable?
```

**Important note:** only apps with should use this method. Otherwise, a `SecurityException` will be thrown.

Equivalent to `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getFastDrawable(kotlin.Int)`.
. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_EXTERNAL_STORAGE:kotlin.String` or android.Manifest.permission.READ_WALLPAPER_INTERNAL

| Parameters ||
|---|---|
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The `FLAG_*` identifier of a valid wallpaper type. Throws IllegalArgumentException if an invalid wallpaper is requested. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#?` | An optimized Drawable object for the requested wallpaper. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | as described in the note |

### removeOnColorsChangedListener

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeOnColorsChangedListener(callback: WallpaperManager.OnColorsChangedListener): Unit
```

Stop listening to color updates.

| Parameters ||
|---|---|
| `callback` | [WallpaperManager.OnColorsChangedListener](../android/app/WallpaperManager.OnColorsChangedListener.md): A callback to unsubscribe. This value cannot be `null`. |

### sendWallpaperCommand

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sendWallpaperCommand(
    windowToken: IBinder!, 
    action: String!, 
    x: Int, 
    y: Int, 
    z: Int, 
    extras: Bundle!
): Unit
```

Send an arbitrary command to the current active wallpaper.

| Parameters ||
|---|---|
| `windowToken` | [IBinder](../android.os/IBinder.md)!: The window who these offsets should be associated with, as returned by `https://developer.android.com/reference/kotlin/android/view/View.html#getWindowToken()`. |
| `action` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Name of the command to perform. This must be a scoped name to avoid collisions, such as "com.mycompany.wallpaper.DOIT". |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Arbitrary integer argument based on command. |
| --- | --- |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Arbitrary integer argument based on command. |
| `z` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Arbitrary integer argument based on command. |
| `extras` | [Bundle](../android.os/Bundle.md)!: Optional additional information for the command, or null. |
| --- | --- |

### setBitmap

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBitmap(bitmap: Bitmap!): Unit
```

Change the current system wallpaper to a bitmap. The given bitmap is converted to a PNG and stored as the wallpaper. On success, the intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WALLPAPER_CHANGED:kotlin.String` is broadcast.

This method is equivalent to calling `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setBitmap(android.graphics.Bitmap,%20android.graphics.Rect,%20kotlin.Boolean)` and passing `null` for the `visibleCrop` rectangle and `true` for the `allowBackup` parameter.

This method requires the caller to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Parameters ||
|---|---|
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md)!: The bitmap to be used as the new system wallpaper. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an error occurs when attempting to set the wallpaper to the provided image. |
| `java.lang.IllegalArgumentException` | if the Bitmap is null |

### setBitmap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBitmap(
    fullImage: Bitmap!, 
    visibleCropHint: Rect!, 
    allowBackup: Boolean
): Int
```

Change the current system wallpaper to a bitmap, specifying a hint about which subrectangle of the full image is to be visible. The OS will then try to best present the given portion of the full image as the static system wallpaper image. On success, the intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WALLPAPER_CHANGED:kotlin.String` is broadcast.

Passing `null` as the `visibleHint` parameter is equivalent to passing (0, 0, `fullImage.getWidth()`, `fullImage.getHeight()`).

This method requires the caller to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Parameters ||
|---|---|
| `fullImage` | [Bitmap](../android.graphics/Bitmap.md)!: A bitmap that will supply the wallpaper imagery. |
| `visibleCropHint` | [Rect](../android.graphics/Rect.md)!: The rectangular subregion of `fullImage` that should be displayed as wallpaper. Passing `null` for this parameter means that the full image should be displayed if possible given the image's and device's aspect ratios, etc. |
| `allowBackup` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the OS is permitted to back up this wallpaper image for restore to a future device; `false` otherwise. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer ID assigned to the newly active wallpaper; or zero on failure. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an error occurs when attempting to set the wallpaper to the provided image. |
| `java.lang.IllegalArgumentException` | If the `visibleCropHint` rectangle is empty or invalid or if the Bitmap is null |

### setBitmap

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBitmap(
    fullImage: Bitmap!, 
    visibleCropHint: Rect!, 
    allowBackup: Boolean, 
    which: Int
): Int
```

Version of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setBitmap(android.graphics.Bitmap,%20android.graphics.Rect,%20kotlin.Boolean)` that allows the caller to specify which of the supported wallpaper categories to set. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Parameters ||
|---|---|
| `fullImage` | [Bitmap](../android.graphics/Bitmap.md)!: A bitmap that will supply the wallpaper imagery. |
| `visibleCropHint` | [Rect](../android.graphics/Rect.md)!: The rectangular subregion of `fullImage` that should be displayed as wallpaper. Passing `null` for this parameter means that the full image should be displayed if possible given the image's and device's aspect ratios, etc. |
| `allowBackup` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the OS is permitted to back up this wallpaper image for restore to a future device; `false` otherwise. |
| --- | --- |
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating which wallpaper(s) to configure with the new imagery. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer ID assigned to the newly active wallpaper; or zero on failure. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |
| `java.lang.IllegalArgumentException` | if the Bitmap is null |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`

### setDisplayPadding

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setDisplayPadding(padding: Rect!): Unit
```

Specify extra padding that the wallpaper should have outside of the display. That is, the given padding supplies additional pixels the wallpaper should extend outside of the display itself.

This method requires the caller to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER_HINTS:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER_HINTS:kotlin.String`

| Parameters ||
|---|---|
| `padding` | [Rect](../android.graphics/Rect.md)!: The number of pixels the wallpaper should extend beyond the display, on its left, top, right, and bottom sides. |

### setResource

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setResource(resid: Int): Unit
```

Change the current system wallpaper to the bitmap in the given resource. The resource is opened as a raw data stream and copied into the wallpaper; it must be a valid PNG or JPEG image. On success, the intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WALLPAPER_CHANGED:kotlin.String` is broadcast.

This method requires the caller to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource ID of the bitmap to be used as the wallpaper image |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an error occurs reverting to the built-in wallpaper. |

### setResource

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setResource(
    resid: Int, 
    which: Int
): Int
```

Version of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setResource(kotlin.Int)` that allows the caller to specify which of the supported wallpaper categories to set. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Parameters ||
|---|---|
| `resid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource ID of the bitmap to be used as the wallpaper image |
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating which wallpaper(s) to configure with the new imagery. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer ID assigned to the newly active wallpaper; or zero on failure. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`

### setStream

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStream(bitmapData: InputStream!): Unit
```

Change the current system wallpaper to a specific byte stream. The give InputStream is copied into persistent storage and will now be used as the wallpaper. Currently it must be either a JPEG or PNG image. On success, the intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WALLPAPER_CHANGED:kotlin.String` is broadcast.

This method is equivalent to calling `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setStream(java.io.InputStream,%20android.graphics.Rect,%20kotlin.Boolean)` and passing `null` for the `visibleCrop` rectangle and `true` for the `allowBackup` parameter.

This method requires the caller to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Parameters ||
|---|---|
| `bitmapData` | [InputStream](../java.io/InputStream.md)!: A stream containing the raw data to install as a wallpaper. This data can be in any format handled by `https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder.html#`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an error occurs when attempting to set the wallpaper based on the provided image data. |

### setStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStream(
    bitmapData: InputStream!, 
    visibleCropHint: Rect!, 
    allowBackup: Boolean
): Int
```

Change the current system wallpaper to a specific byte stream, specifying a hint about which subrectangle of the full image is to be visible. The OS will then try to best present the given portion of the full image as the static system wallpaper image. The data from the given InputStream is copied into persistent storage and will then be used as the system wallpaper. Currently the data must be either a JPEG or PNG image. On success, the intent `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_WALLPAPER_CHANGED:kotlin.String` is broadcast.

This method requires the caller to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Parameters ||
|---|---|
| `bitmapData` | [InputStream](../java.io/InputStream.md)!: A stream containing the raw data to install as a wallpaper. This data can be in any format handled by `https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder.html#`. |
| `visibleCropHint` | [Rect](../android.graphics/Rect.md)!: The rectangular subregion of the streamed image that should be displayed as wallpaper. Passing `null` for this parameter means that the full image should be displayed if possible given the image's and device's aspect ratios, etc. |
| `allowBackup` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the OS is permitted to back up this wallpaper image for restore to a future device; `false` otherwise. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer ID assigned to the newly active wallpaper; or zero on failure. |

| Exceptions ||
|---|---|
| `java.io.IOException` | If an error occurs when attempting to set the wallpaper based on the provided image data. |
| `java.lang.IllegalArgumentException` | If the `visibleCropHint` rectangle is empty or invalid. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getWallpaperId(kotlin.Int)`

### setStream

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStream(
    bitmapData: InputStream!, 
    visibleCropHint: Rect!, 
    allowBackup: Boolean, 
    which: Int
): Int
```

Version of `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#setStream(java.io.InputStream,%20android.graphics.Rect,%20kotlin.Boolean)` that allows the caller to specify which of the supported wallpaper categories to set. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER:kotlin.String`

| Parameters ||
|---|---|
| `bitmapData` | [InputStream](../java.io/InputStream.md)!: A stream containing the raw data to install as a wallpaper. This data can be in any format handled by `https://developer.android.com/reference/kotlin/android/graphics/BitmapRegionDecoder.html#`. |
| `visibleCropHint` | [Rect](../android.graphics/Rect.md)!: The rectangular subregion of the streamed image that should be displayed as wallpaper. Passing `null` for this parameter means that the full image should be displayed if possible given the image's and device's aspect ratios, etc. |
| `allowBackup` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if the OS is permitted to back up this wallpaper image for restore to a future device; `false` otherwise. |
| --- | --- |
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Flags indicating which wallpaper(s) to configure with the new imagery. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer ID assigned to the newly active wallpaper; or zero on failure. |

| Exceptions ||
|---|---|
| `java.io.IOException` | |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getWallpaperId(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int`

### setWallpaperOffsetSteps

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWallpaperOffsetSteps(
    xStep: Float, 
    yStep: Float
): Unit
```

For applications that use multiple virtual screens showing a wallpaper, specify the step size between virtual screens. For example, if the launcher has 3 virtual screens, it would specify an xStep of 0.5, since the X offset for those screens are 0.0, 0.5 and 1.0

| Parameters ||
|---|---|
| `xStep` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X offset delta from one screen to the next one |
| `yStep` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y offset delta from one screen to the next one |

### setWallpaperOffsets

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWallpaperOffsets(
    windowToken: IBinder!, 
    xOffset: Float, 
    yOffset: Float
): Unit
```

Set the display position of the current wallpaper within any larger space, when that wallpaper is visible behind the given window. The X and Y offsets are floating point numbers ranging from 0 to 1, representing where the wallpaper should be positioned within the screen space. These only make sense when the wallpaper is larger than the display.

| Parameters ||
|---|---|
| `windowToken` | [IBinder](../android.os/IBinder.md)!: The window who these offsets should be associated with, as returned by `https://developer.android.com/reference/kotlin/android/view/View.html#getWindowToken()`. |
| `xOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The offset along the X dimension, from 0 to 1. |
| `yOffset` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The offset along the Y dimension, from 0 to 1. |
| --- | --- |

### suggestDesiredDimensions

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun suggestDesiredDimensions(
    minimumWidth: Int, 
    minimumHeight: Int
): Unit
```

For use only by the current home application, to specify the size of wallpaper it would like to use. This allows such applications to have a virtual wallpaper that is larger than the physical screen, matching the size of their workspace.

Calling this method from apps other than the active home app is not guaranteed to work properly. Other apps that supply wallpaper imagery should use `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDesiredMinimumWidth()` and `https://developer.android.com/reference/kotlin/android/app/WallpaperManager#getDesiredMinimumHeight()` and construct a wallpaper that matches those dimensions.

This method requires the caller to hold the permission `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SET_WALLPAPER_HINTS:kotlin.String`.

| Parameters ||
|---|---|
| `minimumWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Desired minimum width |
| `minimumHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Desired minimum height |
