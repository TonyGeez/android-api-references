# MediaProjectionManager

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaProjectionManager

Kotlin| [Java](https://developer.android.com/reference/android/media/projection/MediaProjectionManager "View this page in Java") 
| --- | --- |

```
class MediaProjectionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.projection.MediaProjectionManager](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#) |

Manages the retrieval of certain types of [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) tokens.

<br />

An example flow of starting a media projection will be:
1. Declare a foreground service with the type`mediaProjection`in the`AndroidManifest.xml`.
2. Create an intent by calling [MediaProjectionManager.createScreenCaptureIntent()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent())and pass this intent to [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int)).
3. On getting [Activity.onActivityResult(int, int, Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)), start the foreground service with the type [android.content.pm.ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION:kotlin.Int).
4. Retrieve the media projection token by calling [android.media.projection.MediaProjectionManager#getMediaProjection(int,android.content.Intent)](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#getMediaProjection(kotlin.Int,%20android.content.Intent))with the result code and intent from the [Activity.onActivityResult(int, int, Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent))above.
5. Register a [MediaProjection.Callback](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection.Callback) by calling [android.media.projection.MediaProjection#registerCallback(android.media.projection.MediaProjection.Callback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#registerCallback(android.media.projection.MediaProjection.Callback,%20android.os.Handler)). This is required to receive notifications about when the [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) or captured content changes state. When receiving an \`onStop()\` callback the [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) session has been finished and the client must clean up any resources it is holding, e.g. the [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#) and [Surface](https://developer.android.com/reference/kotlin/android/view/Surface.html#). The MediaProjection may further no longer create any new [VirtualDisplay](https://developer.android.com/reference/kotlin/android/hardware/display/VirtualDisplay.html#) s via [MediaProjection.createVirtualDisplay(String, int,](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20android.hardware.display.VirtualDisplay.Callback,%20android.os.Handler)). Note that the \`onStop()\` callback can be a result of the system stopping MediaProjection due to various reasons. This includes the user stopping the MediaProjection via UI affordances in system-level UI, the screen being locked, or another [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) session starting.
6. Start the screen capture session for media projection by calling [android.media.projection.MediaProjection#createVirtualDisplay(java.lang.String,int,int,int,int,android.view.Surface,android.hardware.display.VirtualDisplay.Callback,android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20android.hardware.display.VirtualDisplay.Callback,%20android.os.Handler)).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | [createScreenCaptureIntent](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent())`()` Returns an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) that**must** be passed to [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))(or similar) in order to start screen capture. |
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | [createScreenCaptureIntent](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent(android.media.projection.MediaProjectionConfig))`(`config:` ` [MediaProjectionConfig](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionConfig)`)` Returns an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) that**must** be passed to [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))(or similar) in order to start screen capture. |
| [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection)? | [getMediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#getMediaProjection(kotlin.Int,%20android.content.Intent))`(`resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultData:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)`)` Retrieves the [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) obtained from a successful screen capture request. |
| --- | --- |

## Public methods

### createScreenCaptureIntent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createScreenCaptureIntent(): Intent
```

Returns an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) that**must** be passed to [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))(or similar) in order to start screen capture. The activity will prompt the user whether to allow screen capture. The result of this activity (received by overriding [onActivityResult(int, int, Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent))) should be passed to [getMediaProjection(int,android.content.Intent)](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#getMediaProjection(kotlin.Int,%20android.content.Intent)).

Identical to calling [createScreenCaptureIntent(android.media.projection.MediaProjectionConfig)](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent(android.media.projection.MediaProjectionConfig))with a [MediaProjectionConfig.createConfigForUserChoice()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionConfig#createConfigForUserChoice()).

Should be used instead of [createScreenCaptureIntent(android.media.projection.MediaProjectionConfig)](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent(android.media.projection.MediaProjectionConfig))when the calling app does not want to customize the activity shown to the user.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | This value cannot be`null`. |

### createScreenCaptureIntent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createScreenCaptureIntent(config: MediaProjectionConfig): Intent
```

Returns an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) that**must** be passed to [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))(or similar) in order to start screen capture. Customizes the activity and resulting [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) session based up the provided`config`. The activity will prompt the user whether to allow screen capture. The result of this activity (received by overriding [onActivityResult(int, int, Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent))) should be passed to [getMediaProjection(int,android.content.Intent)](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#getMediaProjection(kotlin.Int,%20android.content.Intent)).

If [MediaProjectionConfig](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionConfig) was created from:

- [MediaProjectionConfig.createConfigForDefaultDisplay()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionConfig#createConfigForDefaultDisplay()), then creates an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) for capturing the default display. The activity limits the user's choice to just the display specified.
- [MediaProjectionConfig.createConfigForUserChoice()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionConfig#createConfigForUserChoice()), then creates an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) for deferring which region to capture to the user. This gives the user the same behaviour as calling [createScreenCaptureIntent()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent()). The activity gives the user the choice between [android.view.Display#DEFAULT_DISPLAY](https://developer.android.com/reference/kotlin/android/view/Display.html#DEFAULT_DISPLAY:kotlin.Int), or a different region.

<br />

Should be used instead of [createScreenCaptureIntent()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent())when the calling app wants to customize the activity shown to the user.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [MediaProjectionConfig](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionConfig):Customization for the [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) that this [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) requests the user's consent for. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) | An [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) requesting the user's consent, specialized based upon the given configuration. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if android.media.projection.MediaProjectionConfig#isOwnAppContentProvided() is true but no [AppContentProjectionService](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#) is declared. |

### getMediaProjection

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaProjection(
    resultCode: Int, 
    resultData: Intent
): MediaProjection?
```

Retrieves the [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection) obtained from a successful screen capture request. The result code and data from the request are provided by overriding [onActivityResult(int, int, Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)), which is called after starting an activity using [createScreenCaptureIntent()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent()).

Starting from Android [R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int), if your application requests the [SYSTEM_ALERT_WINDOW](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#SYSTEM_ALERT_WINDOW:kotlin.String) permission, and the user has not explicitly denied it, the permission will be automatically granted until the projection is stopped. The permission allows your app to display user controls on top of the screen being captured.

An app targeting SDK version [Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) or later must invoke`getMediaProjection`and maintain the capture session ([MediaProjection#createVirtualDisplay](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection#createVirtualDisplay(kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.view.Surface,%20android.hardware.display.VirtualDisplay.Callback,%20android.os.Handler))) while running a foreground service. The app must set the [foregroundServiceType](https://developer.android.com/reference/kotlin/android/R.attr.html#foregroundServiceType:kotlin.Int) attribute to [FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION:kotlin.Int) in the [`<service>`](https://developer.android.com/reference/kotlin/guide/topics/manifest/service-element) element of the app's manifest file.

For an app targeting SDK version [U](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int) or later, the user must have granted the app with the permission to start a projection, before the app starts a foreground service with the type [android.content.pm.ServiceInfo#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION:kotlin.Int). Additionally, the app must have started the foreground service with that type before calling this API here, or else it'll receive a [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) from this API call, unless it's a privileged app. Apps can request the permission via the [createScreenCaptureIntent()](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjectionManager#createScreenCaptureIntent())and [Activity.startActivityForResult(Intent, int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#startActivityForResult(android.content.Intent,%20kotlin.Int))(or similar APIs).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result code from [onActivityResult(int, int, Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)). |
| `resultData` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#):The result data from [onActivityResult(int, int, Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)). This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MediaProjection](https://developer.android.com/reference/kotlin/android/media/projection/MediaProjection)? | The media projection obtained from a successful screen capture request, or null if the result of the screen capture request is not [RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int). |

| Exceptions ||
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | On pre- [Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) devices if a previously obtained`MediaProjection`from the same`resultData`has not yet been stopped. |
| `java.lang.SecurityException` | On [Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int)+ devices if not invoked from a foreground service with type [FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION](https://developer.android.com/reference/kotlin/android/content/pm/ServiceInfo.html#FOREGROUND_SERVICE_TYPE_MEDIA_PROJECTION:kotlin.Int), unless caller is a privileged app. |

**See Also**
