# EmbeddedPhotoPickerProvider

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions)

# EmbeddedPhotoPickerProvider

Kotlin| [Java](https://developer.android.com/reference/android/widget/photopicker/EmbeddedPhotoPickerProvider "View this page in Java") 
| --- | --- |

```
interface EmbeddedPhotoPickerProvider
```

| [android.widget.photopicker.EmbeddedPhotoPickerProvider](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider#) |

This interface provides an api that callers can use to get a session of embedded PhotoPicker ([EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession)).

Callers can get instance of this class using [EmbeddedPhotoPickerProviderFactory.create(Context)](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProviderFactory#create(android.content.Context)).

Under the hood, a service connection with photopicker is established by the implementation of this api. To help establish this connection, a caller must include in their Manifest: 

```kotlin
<code>&lt;queries&gt;
    &lt;intent&gt;
        &lt;action android:name="com.android.photopicker.core.embedded.EmbeddedService.BIND"/&gt;
    &lt;/intent&gt;
  &lt;/queries&gt;
  </code>
```

When a session opens successfully, they would receive an instance of [EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession) and [android.view.SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#) via the [api](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient#onSessionOpened(android.widget.photopicker.EmbeddedPhotoPickerSession))

Callers pass an instance of [EmbeddedPhotoPickerClient](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient) which is used by service to notify about different events (like sessionError, uri granted/revoked etc) to them. One-to-one relationship of client to session must be maintained by a caller i.e. they shouldn't reuse same callback for more than one openSession requests.

The [EmbeddedPhotoPickerSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerSession) instance can be used to notify photopicker about different events (like resize, configChange etc).

This api is supported on api versions Android U+.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openSession](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerProvider#openSession(android.os.IBinder,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.widget.photopicker.EmbeddedPhotoPickerFeatureInfo,%20java.util.concurrent.Executor,%20android.widget.photopicker.EmbeddedPhotoPickerClient))`(`hostToken:` ` [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)`, `displayId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `featureInfo:` ` [EmbeddedPhotoPickerFeatureInfo](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo)`, `clientExecutor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [EmbeddedPhotoPickerClient](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient)`)` Open a new session for displaying content with an initial size of width x height pixels. |

## Public methods

### openSession

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 15](https://developer.android.com/sdkExtensions) 

```
abstract fun openSession(
    hostToken: IBinder, 
    displayId: Int, 
    width: Int, 
    height: Int, 
    featureInfo: EmbeddedPhotoPickerFeatureInfo, 
    clientExecutor: Executor, 
    callback: EmbeddedPhotoPickerClient
): Unit
```

Open a new session for displaying content with an initial size of width x height pixels. [EmbeddedPhotoPickerClient](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient) will receive all incoming communication from the PhotoPicker. All incoming calls to [EmbeddedPhotoPickerClient](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient) will be made through the provided`clientExecutor`

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `hostToken` | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#):Token used for constructing [android.view.SurfaceControlViewHost](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.html#). Use [AttachedSurfaceControl.getInputTransferToken()](https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.html#getInputTransferToken())to get token of attached [android.view.SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#). This value cannot be`null`. |
| `displayId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Application display id. Use [DisplayManager.getDisplays()](https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplays())to get the id. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):width of the view, in pixels. |
| --- | --- |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):height of the view, in pixels. |
| `featureInfo` | [EmbeddedPhotoPickerFeatureInfo](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo): [EmbeddedPhotoPickerFeatureInfo](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerFeatureInfo) object containing all the required features for the given session. This value cannot be`null`. |
| `clientExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) to invoke callbacks. This value cannot be`null`. |
| --- | --- |
| `callback` | [EmbeddedPhotoPickerClient](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient): [EmbeddedPhotoPickerClient](https://developer.android.com/reference/kotlin/android/widget/photopicker/EmbeddedPhotoPickerClient) object to receive callbacks from photopicker. This value cannot be`null`. |
