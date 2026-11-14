# MediaProjectionManager

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaProjectionManager

Kotlin| [Java](../android/media/projection/MediaProjectionManager.md) 
| --- | --- |

```
class MediaProjectionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.projection.MediaProjectionManager](../android/media/projection/MediaProjectionManager.md) |

Manages the retrieval of certain types of [MediaProjection](../android/media/projection/MediaProjection.md) tokens.

<br />

An example flow of starting a media projection will be:
1. Declare a foreground service with the type`mediaProjection`in the`AndroidManifest.xml`.
2. Create an intent by calling [MediaProjectionManager.createScreenCaptureIntent()](../android/media/projection/MediaProjectionManager.md))and pass this intent to [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md)).
3. On getting [Activity.onActivityResult(int, int, Intent)](../android/app/Activity.md)), start the foreground service with the type [android.content.pm.ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION](../android/content/pm/ServiceInfo.md).
4. Retrieve the media projection token by calling [android.media.projection.MediaProjectionManager#getMediaProjection(int,android.content.Intent)](../android/media/projection/MediaProjectionManager.md))with the result code and intent from the [Activity.onActivityResult(int, int, Intent)](../android/app/Activity.md))above.
5. Register a [MediaProjection.Callback](../android/media/projection/MediaProjection.Callback.md) by calling [android.media.projection.MediaProjection#registerCallback(android.media.projection.MediaProjection.Callback,android.os.Handler)](../android/media/projection/MediaProjection.md)). This is required to receive notifications about when the [MediaProjection](../android/media/projection/MediaProjection.md) or captured content changes state. When receiving an \`onStop()\` callback the [MediaProjection](../android/media/projection/MediaProjection.md) session has been finished and the client must clean up any resources it is holding, e.g. the [VirtualDisplay](../android/hardware/display/VirtualDisplay.md) and [Surface](../android/view/Surface.md). The MediaProjection may further no longer create any new [VirtualDisplay](../android/hardware/display/VirtualDisplay.md) s via [MediaProjection.createVirtualDisplay(String, int,](../android/media/projection/MediaProjection.md)). Note that the \`onStop()\` callback can be a result of the system stopping MediaProjection due to various reasons. This includes the user stopping the MediaProjection via UI affordances in system-level UI, the screen being locked, or another [MediaProjection](../android/media/projection/MediaProjection.md) session starting.
6. Start the screen capture session for media projection by calling [android.media.projection.MediaProjection#createVirtualDisplay(java.lang.String,int,int,int,int,android.view.Surface,android.hardware.display.VirtualDisplay.Callback,android.os.Handler)](../android/media/projection/MediaProjection.md)).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](../android/content/Intent.md) | [createScreenCaptureIntent](../android/media/projection/MediaProjectionManager.md))`()` Returns an [Intent](../android/content/Intent.md) that**must** be passed to [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))(or similar) in order to start screen capture. |
| [Intent](../android/content/Intent.md) | [createScreenCaptureIntent](../android/media/projection/MediaProjectionManager.md))`(`config:` ` [MediaProjectionConfig](../android/media/projection/MediaProjectionConfig.md)`)` Returns an [Intent](../android/content/Intent.md) that**must** be passed to [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))(or similar) in order to start screen capture. |
| [MediaProjection](../android/media/projection/MediaProjection.md)? | [getMediaProjection](../android/media/projection/MediaProjectionManager.md))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultData:` ` [Intent](../android/content/Intent.md)`)` Retrieves the [MediaProjection](../android/media/projection/MediaProjection.md) obtained from a successful screen capture request. |
| --- | --- |

## Public methods

### createScreenCaptureIntent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createScreenCaptureIntent(): Intent
```

Returns an [Intent](../android/content/Intent.md) that**must** be passed to [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))(or similar) in order to start screen capture. The activity will prompt the user whether to allow screen capture. The result of this activity (received by overriding [onActivityResult(int, int, Intent)](../android/app/Activity.md))) should be passed to [getMediaProjection(int,android.content.Intent)](../android/media/projection/MediaProjectionManager.md)).

Identical to calling [createScreenCaptureIntent(android.media.projection.MediaProjectionConfig)](../android/media/projection/MediaProjectionManager.md))with a [MediaProjectionConfig.createConfigForUserChoice()](../android/media/projection/MediaProjectionConfig.md)).

Should be used instead of [createScreenCaptureIntent(android.media.projection.MediaProjectionConfig)](../android/media/projection/MediaProjectionManager.md))when the calling app does not want to customize the activity shown to the user.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [Intent](../android/content/Intent.md) | This value cannot be`null`. |

### createScreenCaptureIntent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createScreenCaptureIntent(config: MediaProjectionConfig): Intent
```

Returns an [Intent](../android/content/Intent.md) that**must** be passed to [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))(or similar) in order to start screen capture. Customizes the activity and resulting [MediaProjection](../android/media/projection/MediaProjection.md) session based up the provided`config`. The activity will prompt the user whether to allow screen capture. The result of this activity (received by overriding [onActivityResult(int, int, Intent)](../android/app/Activity.md))) should be passed to [getMediaProjection(int,android.content.Intent)](../android/media/projection/MediaProjectionManager.md)).

If [MediaProjectionConfig](../android/media/projection/MediaProjectionConfig.md) was created from:

- [MediaProjectionConfig.createConfigForDefaultDisplay()](../android/media/projection/MediaProjectionConfig.md)), then creates an [Intent](../android/content/Intent.md) for capturing the default display. The activity limits the user's choice to just the display specified.
- [MediaProjectionConfig.createConfigForUserChoice()](../android/media/projection/MediaProjectionConfig.md)), then creates an [Intent](../android/content/Intent.md) for deferring which region to capture to the user. This gives the user the same behaviour as calling [createScreenCaptureIntent()](../android/media/projection/MediaProjectionManager.md)). The activity gives the user the choice between [android.view.Display#DEFAULT_DISPLAY](../android/view/Display.md), or a different region.

<br />

Should be used instead of [createScreenCaptureIntent()](../android/media/projection/MediaProjectionManager.md))when the calling app wants to customize the activity shown to the user.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [MediaProjectionConfig](../android/media/projection/MediaProjectionConfig.md):Customization for the [MediaProjection](../android/media/projection/MediaProjection.md) that this [Intent](../android/content/Intent.md) requests the user's consent for. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](../android/content/Intent.md) | An [Intent](../android/content/Intent.md) requesting the user's consent, specialized based upon the given configuration. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if android.media.projection.MediaProjectionConfig#isOwnAppContentProvided() is true but no [AppContentProjectionService](../android/media/projection/MediaProjectionManager.md) is declared. |

### getMediaProjection

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaProjection(
    resultCode: Int, 
    resultData: Intent
): MediaProjection?
```

Retrieves the [MediaProjection](../android/media/projection/MediaProjection.md) obtained from a successful screen capture request. The result code and data from the request are provided by overriding [onActivityResult(int, int, Intent)](../android/app/Activity.md)), which is called after starting an activity using [createScreenCaptureIntent()](../android/media/projection/MediaProjectionManager.md)).

Starting from Android [R](../android/os/Build.VERSION_CODES.md), if your application requests the [SYSTEM_ALERT_WINDOW](../android/Manifest.permission.md) permission, and the user has not explicitly denied it, the permission will be automatically granted until the projection is stopped. The permission allows your app to display user controls on top of the screen being captured.

An app targeting SDK version [Q](../android/os/Build.VERSION_CODES.md) or later must invoke`getMediaProjection`and maintain the capture session ([MediaProjection#createVirtualDisplay](../android/media/projection/MediaProjection.md))) while running a foreground service. The app must set the [foregroundServiceType](../android/R.attr.md) attribute to [FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION](../android/content/pm/ServiceInfo.md) in the [`<service>`](../guide/topics/manifest/service-element.md) element of the app's manifest file.

For an app targeting SDK version [U](../android/os/Build.VERSION_CODES.md) or later, the user must have granted the app with the permission to start a projection, before the app starts a foreground service with the type [android.content.pm.ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION](../android/content/pm/ServiceInfo.md). Additionally, the app must have started the foreground service with that type before calling this API here, or else it'll receive a [SecurityException](../java/lang/SecurityException.md) from this API call, unless it's a privileged app. Apps can request the permission via the [createScreenCaptureIntent()](../android/media/projection/MediaProjectionManager.md))and [Activity.startActivityForResult(Intent, int)](../android/app/Activity.md))(or similar APIs).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result code from [onActivityResult(int, int, Intent)](../android/app/Activity.md)). |
| `resultData` | [Intent](../android/content/Intent.md):The result data from [onActivityResult(int, int, Intent)](../android/app/Activity.md)). This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MediaProjection](../android/media/projection/MediaProjection.md)? | The media projection obtained from a successful screen capture request, or null if the result of the screen capture request is not [RESULT_OK](../android/app/Activity.md). |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | On pre- [Q](../android/os/Build.VERSION_CODES.md) devices if a previously obtained`MediaProjection`from the same`resultData`has not yet been stopped. |
| `java.lang.SecurityException` | On [Q](../android/os/Build.VERSION_CODES.md)+ devices if not invoked from a foreground service with type [FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION](../android/content/pm/ServiceInfo.md), unless caller is a privileged app. |

**See Also**
