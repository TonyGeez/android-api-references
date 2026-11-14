# EmbeddedPhotoPickerSession

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# EmbeddedPhotoPickerSession

Kotlin | [Java](https://developer.android.com/reference/android/widget/photopicker/EmbeddedPhotoPickerSession "View this page in Java") 

```
interface EmbeddedPhotoPickerSession
```

| [android.widget.photopicker.EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession#) |

Class that holds the embedded photopicker view wrapped in [SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#) that can be embedded by the caller in their view hierarchy by placing it in a [SurfaceView](https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#) via its [SurfaceView.setChildSurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#setChildSurfacePackage(android.view.SurfaceControlViewHost.SurfacePackage)) api. Callers of [EmbeddedPhotoPickerProvider.openSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider#openSession(android.os.IBinder,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.widget.photopicker.EmbeddedPhotoPickerFeatureInfo,%20java.util.concurrent.Executor,%20android.widget.photopicker.EmbeddedPhotoPickerClient)) will asynchronously receive instance of this class from the service upon its successful execution via [EmbeddedPhotoPickerClient.onSessionOpened](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient#onSessionOpened(android.widget.photopicker.EmbeddedPhotoPickerSession)) callback.

Instance of this class can be then used by callers to notify PhotoPicker about different events for service to act upon them.

When a session is no longer being used, it should be closed by callers to help system release the resources.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession#close())`()` Close the session, i. |
| abstract [SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#) | [getSurfacePackage](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession#getSurfacePackage())`()` Returns the [SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#) that contains view representing embedded picker. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyConfigurationChanged](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession#notifyConfigurationChanged(android.content.res.Configuration))`(`configuration:` ` [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#)`)` Notifies photopicker that host side configuration has changed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyPhotoPickerExpanded](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession#notifyPhotoPickerExpanded(kotlin.Boolean))`(`isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notify that user switched photopicker between expanded/collapsed state. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyResized](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession#notifyResized(kotlin.Int,%20kotlin.Int))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify that caller's presentation area has changed and photopicker's dimensions should change accordingly. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyVisibilityChanged](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession#notifyVisibilityChanged(kotlin.Boolean))`(`isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notify that embedded photopicker view is visible or not to the user. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestRevokeUriPermission](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession#requestRevokeUriPermission(kotlin.collections.MutableList))`(`uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!>`)` Notify that the user deselected some items. |

## Public methods

### close

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun close(): Unit
```

Close the session, i.e. photopicker will release resources associated with this session. Any further notifications to this Session will be ignored by the service. 

### getSurfacePackage

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun getSurfacePackage(): SurfaceControlViewHost.SurfacePackage
```

Returns the [SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#) that contains view representing embedded picker.

Callers can attach this view in their hierarchy using [SurfaceView.setChildSurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceView.html#setChildSurfacePackage(android.view.SurfaceControlViewHost.SurfacePackage)) api.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#) | This value cannot be `null`. |

### notifyConfigurationChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun notifyConfigurationChanged(configuration: Configuration): Unit
```

Notifies photopicker that host side configuration has changed.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configuration` | [Configuration](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#): new configuration of caller This value cannot be `null`. |

### notifyPhotoPickerExpanded

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun notifyPhotoPickerExpanded(isExpanded: Boolean): Unit
```

Notify that user switched photopicker between expanded/collapsed state.

Some photopicker features (like Profile selector, Album grid etc.) are only shown in full/expanded view and are hidden in collapsed view.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| `isExpanded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): true if expanded, false if collapsed. |

### notifyResized

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun notifyResized(
    width: Int, 
    height: Int
): Unit
```

Notify that caller's presentation area has changed and photopicker's dimensions should change accordingly.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): width of the view, in pixels |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): height of the view, in pixels |

### notifyVisibilityChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun notifyVisibilityChanged(isVisible: Boolean): Unit
```

Notify that embedded photopicker view is visible or not to the user.

This helps photopicker to close upstream work and manage the lifecycle of this Session instance.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `isVisible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True if view visible to the user, false if not. |

### requestRevokeUriPermission

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun requestRevokeUriPermission(uris: MutableList<Uri!>): Unit
```

Notify that the user deselected some items.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>: The [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) list of the deselected items. This value cannot be `null`. |
