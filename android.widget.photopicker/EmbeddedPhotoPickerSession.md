# EmbeddedPhotoPickerSession

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# EmbeddedPhotoPickerSession

Kotlin | [Java](EmbeddedPhotoPickerSession.md) 
| --- | --- |

```
interface EmbeddedPhotoPickerSession
```

| [android.widget.photopicker.EmbeddedPhotoPickerSession](EmbeddedPhotoPickerSession.md) |

Class that holds the embedded photopicker view wrapped in [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) that can be embedded by the caller in their view hierarchy by placing it in a [SurfaceView](../android.view/SurfaceView.md) via its [SurfaceView.setChildSurfacePackage](../android.view/SurfaceView.md)) api. Callers of [EmbeddedPhotoPickerProvider.openSession](EmbeddedPhotoPickerProvider.md)) will asynchronously receive instance of this class from the service upon its successful execution via [EmbeddedPhotoPickerClient.onSessionOpened](EmbeddedPhotoPickerClient.md)) callback.

Instance of this class can be then used by callers to notify PhotoPicker about different events for service to act upon them.

When a session is no longer being used, it should be closed by callers to help system release the resources.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](EmbeddedPhotoPickerSession.md))`()` Close the session, i. |
| abstract [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) | [getSurfacePackage](EmbeddedPhotoPickerSession.md))`()` Returns the [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) that contains view representing embedded picker. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyConfigurationChanged](EmbeddedPhotoPickerSession.md))`(`configuration:` ` [Configuration](../android.content.res/Configuration.md)`)` Notifies photopicker that host side configuration has changed. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyPhotoPickerExpanded](EmbeddedPhotoPickerSession.md))`(`isExpanded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notify that user switched photopicker between expanded/collapsed state. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyResized](EmbeddedPhotoPickerSession.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify that caller's presentation area has changed and photopicker's dimensions should change accordingly. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyVisibilityChanged](EmbeddedPhotoPickerSession.md))`(`isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notify that embedded photopicker view is visible or not to the user. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestRevokeUriPermission](EmbeddedPhotoPickerSession.md))`(`uris:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Uri](../android.net/Uri.md)!>`)` Notify that the user deselected some items. |

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

Returns the [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) that contains view representing embedded picker.

Callers can attach this view in their hierarchy using [SurfaceView.setChildSurfacePackage](../android.view/SurfaceView.md)) api.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md) | This value cannot be `null`. |

### notifyConfigurationChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun notifyConfigurationChanged(configuration: Configuration): Unit
```

Notifies photopicker that host side configuration has changed.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `configuration` | [Configuration](../android.content.res/Configuration.md): new configuration of caller This value cannot be `null`. |

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
| `uris` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](../android.net/Uri.md)!\>: The [Uri](../android.net/Uri.md) list of the deselected items. This value cannot be `null`. |
